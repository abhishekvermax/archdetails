---
title: Understanding the Spark Shuffle
subsection: Spark
order: 10
summary: Why the shuffle exists, what it costs, and the three ways to avoid it.
---

Delete this file once you've written a real one. It exists to show the pattern.

## The only frontmatter you need

Two lines:

```yaml
---
title: Understanding the Spark Shuffle
---
```

Everything else is optional:

| Field | Does what |
|---|---|
| `subsection` | Groups entries under a heading inside the section |
| `order` | Lower numbers sort first. Defaults to 50. |
| `summary` | Used for the page description and search results |

## Adding a new entry

Drop a `.md` file into any section folder. That's the whole process — no
index to update, no date in the filename, no config change.

```
_data-engineering/understanding-the-spark-shuffle.md
      ↓
/architect/data-engineering/understanding-the-spark-shuffle/
```

## What renders

Headings, lists, tables, blockquotes and fenced code blocks are all styled
by `assets/css/main.css`. Syntax highlighting comes from Rouge:

```scala
val skewed = orders
  .withColumn("salt", (rand() * 16).cast("int"))
  .repartition($"customer_id", $"salt")
```

> Pull quotes get a rule in the accent colour.

Nothing in this file is framework-specific. If you migrate off Jekyll later,
the markdown moves as-is.
