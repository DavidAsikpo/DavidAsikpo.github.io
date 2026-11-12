---
title: "How Spark Actually Executes a Join: Broadcast vs. Sort-Merge"
date: 2026-11-12T00:00:00+01:00
draft: false
author: "David Asikpo"
tags:
  - Databricks
  - Apache Spark
  - PySpark
  - Data Engineering
  - Joins
image: /images/py.png
description: "A local, hands-on walkthrough of broadcast and sort-merge joins in PySpark, with no cluster required."
toc: true
---

Learning Databricks and Spark joins, and still guessing why your job is slow? You don't need a cluster to find out.

I built a local, hands-on walkthrough of how Spark executes a join, broadcast versus shuffle (sort-merge), using nothing but a laptop and PySpark in local mode. No Databricks, no cloud cluster, just the mechanics made visible.

## The core idea

Spark has two fundamentally different ways to join data.

- **Broadcast join:** Spark copies the small table to every executor, and each task does the match locally. There is no network shuffle, so it is nearly free.
- **Sort-merge join:** Spark shuffles both sides across the cluster by key, sorts them, then merges. It moves your entire dataset across the wire.

Most people let Spark's `autoBroadcastJoinThreshold` decide silently. That works until Spark guesses wrong on a table that isn't actually small, and the job (or the driver) pays for it.

You can see which strategy Spark picked by reading the physical plan:

```python
from pyspark.sql.functions import broadcast

# Ask Spark to broadcast the small side
joined = big_df.join(broadcast(small_df), "key")

# The plan shows BroadcastHashJoin or SortMergeJoin
joined.explain()
```

## Three things that became concrete

Working through this hands-on, a few ideas stopped being theory.

### 1. A broadcast join can't preserve unmatched rows from the broadcast side

Spark scans one side row by row, while the other side is copied whole to every task. Because no single task ever sees the complete picture of the broadcast side, it can't tell which of its rows went unmatched across the whole dataset. This isn't a limitation to work around. It's structural.

### 2. A broadcast hint on a join type that can't support it is silently ignored

Put a broadcast hint on a join type that can't use it, such as a full outer join, and your job doesn't crash. Spark quietly ignores the hint and falls back to a shuffle. If you assumed you were getting a broadcast, you'd never know unless you checked the plan.

### 3. Skew doesn't show up until you look

Say one key holds 30% of your rows. A sort-merge join's "evenly split work" turns into one task doing most of the job while the rest finish early. Everything looks fine in the aggregate numbers, and the problem only appears when you inspect individual tasks.

## Try it yourself

If this isn't clear enough, the hands-on walkthrough is here: [Spark joins walkthrough](https://lnkd.in/egAjVqH8). Work through it yourself, and feel free to get in touch and tell me how your team decides between broadcast and shuffle in production.

Thanks to [Narender Kumar](https://www.linkedin.com/in/narender-kumar91/), whose videos were a valuable source for this.

