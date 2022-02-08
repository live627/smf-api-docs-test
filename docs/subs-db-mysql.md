---
layout: default
group: func
navtitle: Subs-Db-mysql.php
title: ./Sources/Subs-Db-mysql.php
count: 22
---
* auto-gen TOC:
{:toc}
### smf_db_initiate

```php
function smf_db_initiate(string $db_server, string $db_name, string $db_user, string $db_passwd, string $db_prefix, array $db_options = array()): ?resource
```
Maps the implementations in this file (smf_db_function_name)
 to the $smcFunc['db_function_name'] variable.



Type|Parameter|Description
---|---|---
`string`|`$db_server`|The database server
`string`|`$db_name`|The name of the database
`string`|`$db_user`|The database username
`string`|`$db_passwd`|The database password
`string`|`$db_prefix`|The table prefix
`array`|`$db_options`|An array of database options

### db_extend

```php
function db_extend(string $type = 'extra'): void
```
Extend the database functionality. It calls the respective file's init
to add the implementations in that file to $smcFunc array.



Type|Parameter|Description
---|---|---
`string`|`$type`|Indicates which additional file to load. ('extra', 'packages')

### db_fix_prefix

```php
function db_fix_prefix(string &$db_prefix, string $db_name): void
```
Fix up the prefix so it doesn't require the database to be selected.



Type|Parameter|Description
---|---|---
`string`|` &$db_prefix`|The table prefix
`string`|`$db_name`|The database name

### smf_db_select

```php
function smf_db_select(string $database, object $connection = null): bool
```
Wrap mysqli_select_db so the connection does not need to be specified



Type|Parameter|Description
---|---|---
`string`|` &$database`|The database
`object`|`$connection`|The connection object (if null, $db_connection is used)

### smf_db_get_server_info

```php
function smf_db_get_server_info(object $connection = null): string
```
Wrap mysqli_get_server_info so the connection does not need to be specified



Type|Parameter|Description
---|---|---
`object`|`$connection`|The connection to use (if null, $db_connection is used)

### smf_db_replacement__callback

```php
function smf_db_replacement__callback(array $matches): string
```
Callback for preg_replace_callback on the query.

It allows to replace on the fly a few pre-defined strings, for convenience ('query_see_board', 'query_wanna_see_board', etc), with
their current values from $user_info.
In addition, it performs checks and sanitization on the values sent to the database.

Type|Parameter|Description
---|---|---
`array`|`$matches`|The matches from preg_replace_callback

### smf_db_quote

```php
function smf_db_quote(string $db_string, array $db_values, resource $connection = null): string
```
Just like the db_query, escape and quote a string, but not executing the query.



Type|Parameter|Description
---|---|---
`string`|`$db_string`|The database string
`array`|`$db_values`|An array of values to be injected into the string
`resource`|`$connection`|= null The connection to use (null to use $db_connection)

### smf_db_query

```php
function smf_db_query(string $identifier, string $db_string, array $db_values = array(), resource $connection = null): resource|bool
```
Do a query.  Takes care of errors too.



Type|Parameter|Description
---|---|---
`string`|`$identifier`|An identifier. Only used in Postgres when we need to do things differently...
`string`|`$db_string`|The database string
`array`|`$db_values`|= array() The values to be inserted into the string
`resource`|`$connection`|= null The connection to use (null to use $db_connection)

### smf_db_affected_rows

```php
function smf_db_affected_rows(resource $connection = null): int
```
affected_rows



Type|Parameter|Description
---|---|---
`resource`|`$connection`|A connection to use (if null, $db_connection is used)

### smf_db_insert_id

```php
function smf_db_insert_id(string $table, string $field = null, resource $connection = null): int
```
Gets the ID of the most recently inserted row.



Type|Parameter|Description
---|---|---
`string`|`$table`|The table (only used for Postgres)
`string`|`$field`|= null The specific field (not used here)
`resource`|`$connection`|= null The connection (if null, $db_connection is used)

### smf_db_transaction

```php
function smf_db_transaction(string $type = 'commit', resource $connection = null): bool
```
Do a transaction.



Type|Parameter|Description
---|---|---
`string`|`$type`|The step to perform (i.e. 'begin', 'commit', 'rollback')
`resource`|`$connection`|The connection to use (if null, $db_connection is used)

### smf_db_error

```php
function smf_db_error(string $db_string, object $connection = null): void
```
Database error!
Backtrace, log, try to fix.



Type|Parameter|Description
---|---|---
`string`|`$db_string`|The DB string
`object`|`$connection`|The connection to use (if null, $db_connection is used)

### smf_db_insert

```php
function smf_db_insert(string $method, string $table, array $columns, array $data, array $keys, int $returnmode = 0, object $connection = null): mixed
```
Inserts data into a table



Type|Parameter|Description
---|---|---
`string`|`$method`|The insert method - can be 'replace', 'ignore' or 'insert'
`string`|`$table`|The table we're inserting the data into
`array`|`$columns`|An array of the columns we're inserting the data into. Should contain 'column' => 'datatype' pairs
`array`|`$data`|The data to insert
`array`|`$keys`|The keys for the table, needs to be not empty on replace mode
`int`|``|returnmode 0 = nothing(default), 1 = last row id, 2 = all rows id as array
`object`|`$connection`|The connection to use (if null, $db_connection is used)

### smf_db_error_backtrace

```php
function smf_db_error_backtrace(string $error_message, string $log_message = '', string|bool $error_type = false, string $file = null, int $line = null): void|array
```
This function tries to work out additional error information from a back trace.



Type|Parameter|Description
---|---|---
`string`|`$error_message`|The error message
`string`|`$log_message`|The message to log
`string`&#124;`bool`|`$error_type`|What type of error this is
`string`|`$file`|The file the error occurred in
`int`|`$line`|What line of $file the code which generated the error is on

### smf_db_escape_wildcard_string

```php
function smf_db_escape_wildcard_string(string $string, bool $translate_human_wildcards = false): string
```
Escape the LIKE wildcards so that they match the character and not the wildcard.



Type|Parameter|Description
---|---|---
`string`|`$string`|The string to escape
`bool`|`$translate_human_wildcards`|If true, turns human readable wildcards into SQL wildcards.

### smf_is_resource

```php
function smf_is_resource(mixed $result): bool
```
Validates whether the resource is a valid mysqli instance.

Mysqli uses objects rather than resource. https://bugs.php.net/bug.php?id=42797

Type|Parameter|Description
---|---|---
`mixed`|`$result`|The string to test

### smf_db_fetch_all

```php
function smf_db_fetch_all(resource $request): array
```
Fetches all rows from a result as an array



Type|Parameter|Description
---|---|---
`resource`|`$request`|A MySQL result resource

### smf_db_error_insert

```php
function smf_db_error_insert(array $error_array): void
```
Function to save errors in database in a safe way



Type|Parameter|Description
---|---|---
`array`|``|with keys in this order id_member, log_time, ip, url, message, session, error_type, file, line

### smf_db_custom_order

```php
function smf_db_custom_order(string $field, array $array_values, bool $desc = false): string
```
Function which constructs an optimize custom order string
as an improved alternative to find_in_set()



Type|Parameter|Description
---|---|---
`string`|`$field`|name
`array`|`$array_values`|Field values sequenced in array via order priority. Must cast to int.
`bool`|`$desc`|default false

### smf_db_native_replace

```php
function smf_db_native_replace(): bool
```
Function which return the information if the database supports native replace inserts



### smf_db_cte_support

```php
function smf_db_cte_support(): bool
```
Function which return the information if the database supports cte with recursive



### smf_db_escape_string

```php
function smf_db_escape_string(string $string, resource $connection = null): string
```
Function which return the escaped string



Type|Parameter|Description
---|---|---
`string`|``|the unescaped text
`resource`|`$connection`|= null The connection to use (null to use $db_connection)

