# Neon Drizzle Studio Integration Changelog

This changelog documents updates and fixes for the Drizzle Studio integration that powers the **Tables** page in the Neon Console.

## 1.0.10

- Partitioned tables are shown
- drizzle-studio package version is exposed
- Support generated columns in schema management

## 1.0.9

- Fixed a UI regression that occurred when there was not enough space in a table to resize the last column

## 1.0.8

- Added database metadata to bug report
- Revised dependency tree and reduced bundle size down to 525kb gzipped

## 1.0.7

- Fixed regression with views
- Added `selected-table` props to the component to allow pre-selection of a table
- Added filter by entity type (table/view/materialized view)
- Made the UI loading more progressive

## 1.0.6

- Added response validation from the `drizzle` function

## 1.0.5

- Added `selected-schema` props to the component to allow pre-selection of a schema
- Added support for CHECK constraints in schema viewer

## 1.0.4

- Added database name instead of ID in drizzle function

## 1.0.3

- Array support in schema viewer with ability to select dimensions
- Proper array support in data editor
- Fixed validation of currently selected table (fail gracefully with wrong schema or table name)

## 1.0.2

- Added `ON DELETE`|`ON UPDATE` rules for foreign key constraint
- Fixed deleting table constraints
- Fixed pulling table indexes from db

## 1.0.1

- Added local storage migration

## 1.0.0

- Added the ability to create/alter/drop schemas
- Added the ability to create/alter tables
- Added the ability to create/alter views
- Added the ability to create enums
- Added the ability to refresh db schema
- Improved dropdowns
- Improved style customization

## 0.0.20

- Slot `toolbar-bottom-panel` renamed to `callout` and added when table is not selected.

## 0.0.19

- Added identity columns and generated columns support.

## 0.0.18

- Added `toolbar-bottom-panel` slot into toolbar.

## 0.0.17

- Added flat schema capability (show tables without grouping by schema).
- Fixed display of `bytea` data and added the ability to change the display type to hex or utf8.
- Fixed deletion of materialized views.
- Fixed limit reset when applying a filter.
- Fixed an issue with switching between tables with the same names in schemas.

## 0.0.16

- Fixed an issue where updating a column value in one row via the table editor updated the same column value in other rows.
