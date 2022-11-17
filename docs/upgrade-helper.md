---
layout: default
group: func
navtitle: upgrade-helper.php
title: ./upgrade-helper.php
count: 16
---
* auto-gen TOC:
{:toc}
### upgrade_clean_cache

```php
function upgrade_clean_cache(): void
```
Clean the cache using the SMF 2.1 CacheAPI.

If coming from SMF 2.0 and below it should wipe the cache using the SMF backend.

### getMemberGroups

```php
function getMemberGroups(): array
```
Returns a list of member groups. Used to upgrade 1.0 and 1.1.



### makeFilesWritable

```php
function makeFilesWritable(??? &$files): bool
```
Make files writable. First try to use regular chmod, but if that fails, try to use FTP.



Type|Parameter|Description
---|---|---
`null`|`$files`|

### quickFileWritable

```php
function quickFileWritable(string $file): bool
```
The quick version of makeFilesWritable, which does not support FTP.



Type|Parameter|Description
---|---|---
`string`|`$file`|

### deleteFile

```php
function deleteFile(string $file): void
```
Delete a file.  Check permissions first, just in case.



Type|Parameter|Description
---|---|---
`string`|`$file`|

### smf_strtolower

```php
function smf_strtolower(??? $string): string
```
UTF-8 aware strtolower function.



Type|Parameter|Description
---|---|---
`null`|`$string`|

### print_error

```php
function print_error(??? $message, bool $fatal = false): void
```
Prints an error to stderr.



Type|Parameter|Description
---|---|---
`null`|`$message`|
`bool`|`$fatal`|

### throw_error

```php
function throw_error(??? $message): bool
```
Throws a graphical error message.



Type|Parameter|Description
---|---|---
`null`|`$message`|

### smf_mysql_fetch_assoc

```php
function smf_mysql_fetch_assoc(??? $rs): ?array
```




Type|Parameter|Description
---|---|---
`null`|`$rs`|

### smf_mysql_fetch_row

```php
function smf_mysql_fetch_row(??? $rs): ?array
```




Type|Parameter|Description
---|---|---
`null`|`$rs`|

### smf_mysql_free_result

```php
function smf_mysql_free_result(??? $rs): void
```




Type|Parameter|Description
---|---|---
`null`|`$rs`|

### smf_mysql_insert_id

```php
function smf_mysql_insert_id(??? $rs = null): int|string
```




Type|Parameter|Description
---|---|---
`null`|`$rs`|Ignored

### smf_mysql_num_rows

```php
function smf_mysql_num_rows(??? $rs): int
```




Type|Parameter|Description
---|---|---
`null`|`$rs`|

### smf_mysql_real_escape_string

```php
function smf_mysql_real_escape_string(??? $string): void
```




Type|Parameter|Description
---|---|---
`null`|`$string`|

### array_column

```php
function array_column($input, $column_key, $index_key = null)
```
### upgradeCacheSettings

```php
function upgradeCacheSettings(): string
```
Creates the json_encoded array for the current cache option.



