# Drizzle Migration Workflow

1. Confirm the configured dialect and migration output directory.
2. Generate a migration from the intended schema change.
3. Inspect the SQL for table rebuilds, dropped columns, nullability changes, and data loss.
4. Add a backfill or staged migration when existing rows need transformation.
5. Apply to a disposable local database first.
6. Run integration tests against the migrated schema.
7. Back up production data and define rollback or forward-fix steps before release.

Never assume a generated migration is safe simply because generation succeeded.
