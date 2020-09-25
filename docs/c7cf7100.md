---
layout: default
group: func
navtitle: ManageScheduledTasks.php
title: ./Sources/ManageScheduledTasks.php
count: 8
---
* auto-gen TOC:
{:toc}
### ManageScheduledTasks

```php
function ManageScheduledTasks()
```
Scheduled tasks management dispatcher. This function checks permissions and delegates
to the appropriate function based on the sub-action.

Everything here requires admin_forum permission.

Uses ManageScheduledTasks template file
Uses ManageScheduledTasks language file

### ScheduledTasks

```php
function ScheduledTasks()
```
List all the scheduled task in place on the forum.



### list_getScheduledTasks

```php
function list_getScheduledTasks($start, $items_per_page, $sort)
```
Callback function for createList() in ScheduledTasks().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to display per page (not used here)
`string`|`$sort`|A string indicating how to sort things (not used here)

### EditTask

```php
function EditTask()
```
Function for editing a task.



### TaskLog

```php
function TaskLog()
```
Show the log of all tasks that have taken place.

Uses ManageScheduledTasks language file

### list_getTaskLogEntries

```php
function list_getTaskLogEntries($start, $items_per_page, $sort)
```
Callback function for createList() in TaskLog().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to display per page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumTaskLogEntries

```php
function list_getNumTaskLogEntries()
```
Callback function for createList() in TaskLog().



### TaskSettings

```php
function TaskSettings($return_config = false)
```
This handles settings related to scheduled tasks



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config vars. Used in the admin search.

