---
title: "Your LEFT JOIN Might Be an INNER JOIN in Disguise"
date: 2026-11-12T00:30:00+01:00
draft: false
author: "David Asikpo"
tags:
  - SQL
  - Data Engineering
  - Analytics Engineering
  - dbt
  - Joins
image: /images/left.png
description: "Filtering the right table in WHERE quietly turns a LEFT JOIN into an INNER JOIN. Here is why it happens and the one-line fix."
toc: true
---

Your LEFT JOIN might be an INNER JOIN in disguise.

If you filter the right table in `WHERE`, unmatched rows carry `NULL`, the condition fails, and those rows disappear. Move the filter into `ON` and every customer stays.

A small fix, but a big difference in reconciliation reports.

## The problem

This query looks like it keeps every customer:

```sql
SELECT c.customer_id, o.order_id
FROM customers c
LEFT JOIN orders o
  ON o.customer_id = c.customer_id
WHERE o.status = 'completed';
```

It doesn't. A customer with no orders gets `NULL` in every `orders` column. The `WHERE` clause then tests `NULL = 'completed'`, which is not true, so the row is filtered out. Customers without a completed order vanish, and the result behaves like an `INNER JOIN`.

## The fix

Move the filter into the `ON` clause:

```sql
SELECT c.customer_id, o.order_id
FROM customers c
LEFT JOIN orders o
  ON o.customer_id = c.customer_id
 AND o.status = 'completed';
```

Now the filter decides which orders match, instead of which rows survive. Every customer stays, and those without a completed order show `NULL` for the order columns.

## Why it matters

Reconciliation reports depend on the left table staying complete. If customers disappear silently, totals look plausible but don't match the source, and nobody gets an error. A simple check helps: compare the row count of your output against the left table, for example with a dbt test.

## When WHERE is correct

- **Finding unmatched rows:** `WHERE o.order_id IS NULL` is an anti-join, and the filter is intentional.
- **Wanting inner behavior:** if you really want only customers with completed orders, write `INNER JOIN`, so the next reader doesn't have to guess.

Save this for your next code review.