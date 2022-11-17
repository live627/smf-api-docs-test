---
layout: default
group: func
navtitle: cron.php
title: ./cron.php
count: 5
---
* auto-gen TOC:
{:toc}
### fetch_task

```php
function fetch_task(): bool|array
```
The heart of this cron handler.

..

### perform_task

```php
function perform_task(array $task_details): bool|void
```
This actually handles the task



Type|Parameter|Description
---|---|---
`array`|`$task_details`|An array of info about the task

### cleanRequest_cron

```php
function cleanRequest_cron(): void
```
Cleans up the request variables



### smf_error_handler_cron

```php
function smf_error_handler_cron(int $error_level, string $error_string, string $file, int $line): void
```
The error handling function



Type|Parameter|Description
---|---|---
`int`|`$error_level`|One of the PHP error level constants \(see \)
`string`|`$error_string`|The error message
`string`|`$file`|The file where the error occurred
`int`|`$line`|What line of the specified file the error occurred on

### obExit_cron

```php
function obExit_cron(): void
```
The exit function



