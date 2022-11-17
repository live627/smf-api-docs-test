---
layout: default
group: func
navtitle: DbSearch-postgresql.php
title: ./Sources/DbSearch-postgresql.php
count: 5
---
* auto-gen TOC:
{:toc}
### db_search_init

```php
function db_search_init(): void
```
Add the file functions to the $smcFunc array.



### smf_db_search_support

```php
function smf_db_search_support(string $search_type): bool
```
This function will tell you whether this database type supports this search type.



Type|Parameter|Description
---|---|---
`string`|`$search_type`|The search type

### smf_db_search_query

```php
function smf_db_search_query(string $identifier, string $db_string, array $db_values = array(), resource $connection = null): resource
```
Returns the correct query for this search type.



Type|Parameter|Description
---|---|---
`string`|`$identifier`|A query identifier
`string`|`$db_string`|The query text
`array`|`$db_values`|An array of values to pass to $smcFunc\['db\_query'\]
`resource`|`$connection`|The current DB connection resource

### smf_db_create_word_search

```php
function smf_db_create_word_search(string $size): void
```
Highly specific function, to create the custom word index table.



Type|Parameter|Description
---|---|---
`string`|`$size`|The column size type \(int, mediumint \(8\), etc\.\)\. Not used here\.

### smf_db_search_language

```php
function smf_db_search_language(): void
```
Return the language for the textsearch index



