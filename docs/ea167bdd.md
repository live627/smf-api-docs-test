---
layout: default
title: DbSearch-postgresql.php
count: 5
---

# ./Sources/DbSearch-postgresql.php

### db_search_init

```php
function db_search_init()
```
Add the file functions to the $smcFunc array.




### smf_db_search_support

```php
function smf_db_search_support($search_type)
```
This function will tell you whether this database type supports this search type.



Type|Parameter|Name
---|---|---
string|$search_type|The search type

### smf_db_search_query

```php
function smf_db_search_query($identifier, $db_string, $db_values = array(), $connection = null)
```
Returns the correct query for this search type.



Type|Parameter|Name
---|---|---
string|$identifier|A query identifier
string|$db_string|The query text
array|$db_values|An array of values to pass to $smcFunc['db_query']
resource|$connection|The current DB connection resource

### smf_db_create_word_search

```php
function smf_db_create_word_search($size)
```
Highly specific function, to create the custom word index table.



Type|Parameter|Name
---|---|---
string|$size|The column size type (int, mediumint (8), etc.). Not used here.

### smf_db_search_language

```php
function smf_db_search_language()
```
Return the language for the textsearch index




