# Drizzle Schema Patterns

## Schema design checklist
- Primary key strategy is consistent.
- Foreign keys and delete/update actions reflect domain behavior.
- Unique constraints enforce true business uniqueness.
- Indexes support actual filters, joins, and sort orders.
- Timestamps and timezone semantics are explicit.
- Numeric precision is selected deliberately for money and measurements.
- Nullable columns represent genuine optionality.

## Type inference
Use inferred select and insert types from table definitions. Avoid duplicating hand-written types that can drift from the schema.

## Relations vs constraints
Drizzle relation declarations help query relational data. They do not automatically replace physical foreign-key constraints in the database. Define both when referential integrity is required.
