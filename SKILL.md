---
name: drizzle-orm-expert
description: Helps design, query, migrate, and troubleshoot TypeScript applications using Drizzle ORM with explicit schema and SQL reasoning.
---

# Drizzle ORM Expert

Use this skill for Drizzle schema design, typed queries, relations, migrations, transactions, and database integration.

## Workflow
1. Identify database engine, Drizzle version, driver, runtime, and migration strategy.
2. Inspect the existing schema and configuration before editing.
3. Define tables, constraints, indexes, relations, and inferred types.
4. Prefer parameterized query-builder or SQL-template usage.
5. Explain generated SQL for non-trivial queries.
6. Generate migrations and review them before applying to shared or production databases.
7. Test constraints, transaction boundaries, and rollback behavior.

## Rules
- Do not assume relation definitions create database foreign keys.
- Distinguish schema relations from physical constraints.
- Never run destructive migrations without explicit approval and a recovery plan.
- Do not use `push` as an unreviewed production migration strategy.
- Keep database credentials out of source control.
- Avoid N+1 query patterns and select only needed columns.

See `references/schema-patterns.md`, `references/migrations.md`, and `templates/schema-review.md`.
