---
layout: default
group: func
navtitle: DbExtra-postgresql.php
title: ./Sources/DbExtra-postgresql.php
count: 8
---
* auto-gen TOC:
{:toc}
### db_extra_init

```php
function db_extra_init()
```
Add the functions implemented in this file to the $smcFunc array.



### smf_db_backup_table

```php
function smf_db_backup_table($table, $backup_table)
```
Backup $table to $backup_table.



Type|Parameter|Description
---|---|---
`string`|`$table`|The name of the table to backup
`string`|`$backup_table`|The name of the backup table for this table

### smf_db_optimize_table

```php
function smf_db_optimize_table($table)
```
This function optimizes a table.



Type|Parameter|Description
---|---|---
`string`|`$table`|The table to be optimized

### smf_db_list_tables

```php
function smf_db_list_tables($db = false, $filter = false)
```
This function lists all tables in the database.

The listing could be filtered according to $filter.

Type|Parameter|Description
---|---|---
`string&#124;bool`|`$db`|string The database name or false to use the current DB
`string&#124;bool`|`$filter`|String to filter by or false to list all tables

### smf_db_table_sql

```php
function smf_db_table_sql($tableName)
```
Dumps the schema (CREATE) for a table.



Type|Parameter|Description
---|---|---
`string`|`$tableName`|The name of the table

### smf_db_get_version

```php
function smf_db_get_version()
```
Get the version number.



### smf_db_get_vendor

```php
function smf_db_get_vendor()
```
Return PostgreSQL



### smf_db_allow_persistent

```php
function smf_db_allow_persistent()
```
Figures out if persistent connection is allowed



