# Database Optimizer

**Category:** Engineering | **Version:** 1.0.0

Analyzes SQL queries, schema designs, and ORM patterns to find performance bottlenecks. Recommends indexes, query rewrites, and schema improvements.

## What it does

- Identifies missing indexes and N+1 patterns
- Detects full table scans and inefficient JOINs
- Reviews schema design for normalization and type issues
- Works with raw SQL, ORM models, and migration files

## Usage

```
/db-optimizer
/db-optimizer src/db/schema.ts
```

## Tags

`database` `sql` `performance` `optimization` `indexes`
