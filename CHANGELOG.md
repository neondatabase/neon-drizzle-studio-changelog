# Neon Drizzle Studio Integration Changelog

This changelog documents updates and fixes for the Drizzle Studio integration that powers the **Tables** page in the Neon Console.

## 0.0.17

- Added flat schema capability (show tables without grouping by schema).
- Fixed display of `bytea` data and added the ability to change the display type to hex or utf8.
- Fixed deletion of materialized views.
- Fixed limit reset when applying a filter.

## 0.0.16

- Fixed an issue where updating a column value in one row via the table editor updated the same column value in other rows.
