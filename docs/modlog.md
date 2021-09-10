---
layout: default
group: func
navtitle: Modlog.php
title: ./Sources/Modlog.php
count: 3
---
* auto-gen TOC:
{:toc}
### ViewModlog

```php
function ViewModlog()
```
Prepares the information from the moderation log for viewing.

Show the moderation log.
If clearing the log, leaves a message in the log to indicate it was cleared, by whom and when.
Requires the admin_forum permission.
Accessed via ?action=moderate;area=modlog.

Uses Modlog template, main sub-template.

### list_getModLogEntryCount

```php
function list_getModLogEntryCount($query_string = '', $query_params = array(), $log_type = 1, $ignore_boards = false)
```
Get the number of mod log entries.

Callback for createList() in ViewModlog().

Type|Parameter|Description
---|---|---
`string`|`$query_string`|An extra string for the WHERE clause in the query to further filter results
`array`|`$query_params`|An array of parameters for the query_string
`int`|`$log_type`|The log type (1 for mod log, 3 for admin log)
`bool`|`$ignore_boards`|Whether to ignore board restrictions

### list_getModLogEntries

```php
function list_getModLogEntries($start, $items_per_page, $sort, $query_string = '', $query_params = array(), $log_type = 1, $ignore_boards = false)
```
Gets the moderation log entries that match the specified parameters.

Callback for createList() in ViewModlog().

Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results
`string`|`$query_string`|An extra string for the WHERE clause of the query, to further filter results
`array`|`$query_params`|An array of parameters for the query string
`int`|`$log_type`|The log type - 1 for mod log or 3 for admin log
`bool`|`$ignore_boards`|Whether to ignore board restrictions

