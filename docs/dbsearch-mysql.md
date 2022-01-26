---
layout: default
group: func
navtitle: DbSearch-mysql.php
title: ./Sources/DbSearch-mysql.php
count: 3
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
`string`|`$search_type`|The search type.

### smf_db_create_word_search

```php
function smf_db_create_word_search(string $size): void
```
Highly specific function, to create the custom word index table.



Type|Parameter|Description
---|---|---
`string`|`$size`|The size of the desired index.

