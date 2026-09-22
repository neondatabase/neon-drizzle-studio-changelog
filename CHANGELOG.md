# Neon Drizzle Studio Integration Changelog

This changelog documents updates and fixes for the Drizzle Studio integration that powers the **Tables** page in the Neon Console.

## 1.5.3

- Fixed indexes introspection (ARRAY\[...]\).

## 1.5.2

- Fixed foreign key resolution for inaccessible tables.

## 1.5.1

- Added the ability to sort by multiple columns.
- Added `Cmd/Ctrl + A` shortcut for selecting all rows.
- Added `Option/Alt + N` shortcut for adding a new row.
- Added `Option/Alt + F` shortcut for filtering rows.
- Added the ability to copy table creation statements to the clipboard.
- Added the ability to export and copy rows in SQL format (insert statements).
- Reworked header cell sorting functionality.
- Reworked refresh shortcuts: `Cmd/Ctrl + R` refreshes rows, while `Shift + Cmd/Ctrl + R` refreshes schema and rows.
- Restricted the scope of event and keyboard listeners.

## 1.5.0

- Added the ability to copy rows to the clipboard in addition to exporting.
- Added drag-and-drop support for column ordering.
- Added enum values to the filters.
- Fixed DDL export.
- Fixed partitioned indexes regression.
- Improved performance.

## 1.4.3

- Fixed schema introspection failing for non-admin users.

## 1.4.2

- Removed emojis from the error page.
- Fixed index introspection for partitioned tables.

## 1.4.1

- Fixed policies dropping in the table structure.
- Fixed escaping in privileges.

## 1.4.0

- Reworked pagination.
- Added column reordering.
- Added a separate component for sorting (not only via column header clicks).
- Added right-click support on selected cells for copy/paste.
- Added dynamic naming for subviews if they are not explicitly renamed.
- Added filter value validation.
- Improved performance.
- Improved boolean value editor.
- Fixed escaping of names in role alternations.
- Added `entityFilter` prop.
- Fixed insertion of `integer[]` values.

## 1.3.2

- Fixed regression in validation caused by zod upgrade.

## 1.3.1

- Removed the error stack trace from the error page.
- Added a `error-fallback-component` slot for a custom error page.

## 1.3.0

- Fixed issue with uppercase letters in enum column types.
- Fixed issue with adding foreign keys.

## 1.2.9

- Fixed an issue with `json` cell values being copied in the wrong format.

## 1.2.8

- Fixed an issue with displaying `vector` column values.

## 1.2.7

- Enhanced range selection for copying/pasting data between cells.
- Improved performance for tables containing long values.
- Added SQL editor for default values and generated expressions.
- Fixed an issue with multi-dimensional arrays.

## 1.2.6

- Fixed the errors introduced in version `1.2.5` (related to creating and altering entities).

## 1.2.5

- Added initial support for partitioned tables.

## 1.2.4

- Fixed retrieval of foreign keys from the database.
- Fixed handling of bigints.

## 1.2.3

- Fully qualified PostgreSQL system tables and operators when querying the database.
- Disabled the `Superuser` option for roles.
- Removed system roles from the `Privileges` section.
- Made the RLS toggle green when enabled.
- Always show RLS lock symbols on sidebar hover.
- Fixed some issues.

## 1.2.2

- Fixed incorrect sql generation.

## 1.2.1

- Prevent use of non-system functions when querying the database.
- Fixed `RangeError`.

## 1.2.0

- Added support for roles, privileges and policies.
- Introduced a new page (`Database studio`) for managing the full database schema.
- Integrated the introspection and alternation engine from `drizzle-kit`.

## 1.1.4

- The page title section has been replaced by the `page-title` slot.

## 1.1.3

- Fixed loading spinners
- Fixed text selection while sidebar resizing
- Show empty view if the schema is empty
- When create a table, the default schema is the one selected in the sidebar
- Fixed JSONB datatype when exporting to csv
- Added data reload to cmd+R (Also added external function refresh)
- Added aria-label for icon buttons
- Fix relation names

## 1.1.2

- Bundle React

## 1.0.22

- Added a multiline editor.
- Changed JSON editor ui.
- Fixed resizing of columns in Safari browser.
- Fixed a bug where FK constraints were not displayed if CHECK constraints existed.
- Fixed ui bugs with toolbar buttons.
- Fixed saving bug in json cell editor.
- Fixed incorrect `bigserial` value handling.

## 1.0.21

- Added a button to retrieve the database schema.

## 1.0.20

- Added additional context and an identifier to error in the error callback.
- Moved the logic out of the `window` and web component props to prevent XSS, and instead handle it through interactions with `ref`.

## 1.0.19

- Fixed a regression where primary keys were missing.

## 1.0.18

- Fixed foreign key introspection.
- Added `readonly` props to the component.

## 1.0.17

- Fixed export.
- Added export in `xlsx` format.

## 1.0.16

- Fixed JSON editor for `jsonb` columns.

## 1.0.15

- Added `exclude-schemas` props to the component to allow specific schemas.
- Added `exclude-tables` props to the component to allow specific tables.

## 1.0.14

- Fixed a regression where the error dialog would not be displayed if some cell values ​​could not be converted.

## 1.0.13

- Added datepicker and timepicker.
- Added error handling in schema management.
- Added a new setting option for pagination by page.
- Improved error handling for INSERT/UPDATE/DELETE.
- Added `isUnexpected` as the second parameter to `drizzleError` function.
- Added column type to header cell.
- Fixed a bug when an enum had an empty string value.

## 1.0.12

- Fixed `toSorted` bug caused by older browser versions.

## 1.0.11

- Added `uuid`, `cidr`, `inet`, `macaddr` and `macaddr8` data types.
- Added range selection with copy/paste capability.
- Added new setting option for expanding subviews.

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
