---
layout: default
group: func
navtitle: DbPackages-mysql.php
title: ./Sources/DbPackages-mysql.php
count: 13
---
* auto-gen TOC:
{:toc}
### db_packages_init

```php
function db_packages_init()
```
Add the file functions to the $smcFunc array.



### smf_db_create_table

```php
function smf_db_create_table($table_name, $columns, $indexes = array(), $parameters = array(), $if_exists = 'ignore', $error = 'fatal')
```
This function can be used to create a table without worrying about schema
 compatibilities across supported database systems.

- If the table exists will, by default, do nothing.
- Builds table with columns as passed to it - at least one column must be sent.
The columns array should have one sub-array for each column - these sub arrays contain:
	'name' = Column name
	'type' = Type of column - values from (smallint, mediumint, int, text, varchar, char, tinytext, mediumtext, largetext)
	'size' => Size of column (If applicable) - for example 255 for a large varchar, 10 for an int etc.
		If not set SMF will pick a size.
	- 'default' = Default value - do not set if no default required.
	- 'not_null' => Can it be null (true or false) - if not set default will be false.
	- 'auto' => Set to true to make it an auto incrementing column. Set to a numerical value to set from what
		 it should begin counting.
- Adds indexes as specified within indexes parameter. Each index should be a member of $indexes. Values are:
	- 'name' => Index name (If left empty SMF will generate).
	- 'type' => Type of index. Choose from 'primary', 'unique' or 'index'. If not set will default to 'index'.
	- 'columns' => Array containing columns that form part of key - in the order the index is to be created.
- parameters: (None yet)
- if_exists values:
	- 'ignore' will do nothing if the table exists. (And will return true)
	- 'overwrite' will drop any existing table of the same name.
	- 'error' will return false if the table already exists.
	- 'update' will update the table if the table already exists (no change of ai field and only colums with the same name keep the data)

Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to create
`array`|`$columns`|An array of column info in the specified format
`array`|`$indexes`|An array of index info in the specified format
`array`|`$parameters`|Extra parameters. Currently only 'engine', the desired MySQL storage engine, is used.
`string`|`$if_exists`|What to do if the table exists.
`string`|`$error`|

### smf_db_drop_table

```php
function smf_db_drop_table($table_name, $parameters = array(), $error = 'fatal')
```
Drop a table.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to drop
`array`|`$parameters`|Not used at the moment
`string`|`$error`|

### smf_db_add_column

```php
function smf_db_add_column($table_name, $column_info, $parameters = array(), $if_exists = 'update', $error = 'fatal')
```
This function adds a column.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to add the column to
`array`|`$column_info`|An array of column info ({@see \smf_db_create_table})
`array`|`$parameters`|Not used?
`string`|`$if_exists`|What to do if the column exists. If 'update', column is updated.
`string`|`$error`|

### smf_db_remove_column

```php
function smf_db_remove_column($table_name, $column_name, $parameters = array(), $error = 'fatal')
```
Removes a column.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to drop the column from
`string`|`$column_name`|The name of the column to drop
`array`|`$parameters`|Not used?
`string`|`$error`|

### smf_db_change_column

```php
function smf_db_change_column($table_name, $old_column, $column_info)
```
Change a column.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table this column is in
`string`|`$old_column`|The name of the column we want to change
`array`|`$column_info`|An array of info about the "new" column definition (see {@link smf_db_create_table()})

### smf_db_add_index

```php
function smf_db_add_index($table_name, $index_info, $parameters = array(), $if_exists = 'update', $error = 'fatal')
```
Add an index.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to add the index to
`array`|`$index_info`|An array of index info (see {@link smf_db_create_table()})
`array`|`$parameters`|Not used?
`string`|`$if_exists`|What to do if the index exists. If 'update', the definition will be updated.
`string`|`$error`|

### smf_db_remove_index

```php
function smf_db_remove_index($table_name, $index_name, $parameters = array(), $error = 'fatal')
```
Remove an index.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to remove the index from
`string`|`$index_name`|The name of the index to remove
`array`|`$parameters`|Not used?
`string`|`$error`|

### smf_db_calculate_type

```php
function smf_db_calculate_type($type_name, $type_size = null, $reverse = false)
```
Get the schema formatted name for a type.



Type|Parameter|Description
---|---|---
`string`|`$type_name`|The data type (int, varchar, smallint, etc.)
`int`|`$type_size`|The size (8, 255, etc.)
`bool`|`$reverse`|

### smf_db_table_structure

```php
function smf_db_table_structure($table_name)
```
Get table structure.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table

### smf_db_list_columns

```php
function smf_db_list_columns($table_name, $detail = false, $parameters = array())
```
Return column information for a table.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to get column info for
`bool`|`$detail`|Whether or not to return detailed info. If true, returns the column info. If false, just returns the column names.
`array`|`$parameters`|Not used?

### smf_db_list_indexes

```php
function smf_db_list_indexes($table_name, $detail = false, $parameters = array())
```
Get index information.



Type|Parameter|Description
---|---|---
`string`|`$table_name`|The name of the table to get indexes for
`bool`|`$detail`|Whether or not to return detailed info.
`array`|`$parameters`|Not used?

### smf_db_create_query_column

```php
function smf_db_create_query_column($column)
```
Creates a query for a column



Type|Parameter|Description
---|---|---
`array`|`$column`|An array of column info

