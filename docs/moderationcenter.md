---
layout: default
group: func
navtitle: ModerationCenter.php
title: ./Sources/ModerationCenter.php
count: 25
---
* auto-gen TOC:
{:toc}
### ModerationMain

```php
function ModerationMain($dont_call = false)
```
Entry point for the moderation center.



Type|Parameter|Description
---|---|---
`bool`|`$dont_call`|If true, doesn't call the function for the appropriate mod area

### ModerationHome

```php
function ModerationHome()
```
This function basically is the home page of the moderation center.



### ModBlockWatchedUsers

```php
function ModBlockWatchedUsers()
```
Show a list of the most active watched users.



### ModBlockNotes

```php
function ModBlockNotes()
```
Show an area for the moderator to type into.



### ModBlockReportedPosts

```php
function ModBlockReportedPosts()
```
Show a list of the most recent reported posts.



### ModBlockGroupRequests

```php
function ModBlockGroupRequests()
```
Show a list of all the group requests they can see.



### ModBlockReportedMembers

```php
function ModBlockReportedMembers()
```
Show a list of the most recent reported posts.



### ReportedMembers

```php
function ReportedMembers()
```
Browse all the reported users.

..

### ModerateGroups

```php
function ModerateGroups()
```
Act as an entrace for all group related activity.



### ShowNotice

```php
function ShowNotice()
```
Show a notice sent to a user.



### ViewWatchedUsers

```php
function ViewWatchedUsers()
```
View watched users.



### list_getWatchedUserCount

```php
function list_getWatchedUserCount($approve_query)
```
Callback for createList().



Type|Parameter|Description
---|---|---
`string`|`$approve_query`|Not used here

### list_getWatchedUsers

```php
function list_getWatchedUsers($start, $items_per_page, $sort, $approve_query, $dummy)
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort things
`string`|`$approve_query`|A query for approving things. Not used here.
`string`|`$dummy`|Not used here.

### list_getWatchedUserPostsCount

```php
function list_getWatchedUserPostsCount($approve_query)
```
Callback for createList().



Type|Parameter|Description
---|---|---
`string`|`$approve_query`|A query to pull only approved items

### list_getWatchedUserPosts

```php
function list_getWatchedUserPosts($start, $items_per_page, $sort, $approve_query, $delete_boards)
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results (not used here)
`string`|`$approve_query`|A query to only pull approved items
`int[]`|`$delete_boards`|An array containing the IDs of boards we can delete posts in

### ViewWarnings

```php
function ViewWarnings()
```
Entry point for viewing warning related stuff.



### ViewWarningLog

```php
function ViewWarningLog()
```
Simply put, look at the warning log!



### list_getWarningCount

```php
function list_getWarningCount()
```
Callback for createList().



### list_getWarnings

```php
function list_getWarnings($start, $items_per_page, $sort)
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### ViewWarningTemplates

```php
function ViewWarningTemplates()
```
Load all the warning templates.



### list_getWarningTemplateCount

```php
function list_getWarningTemplateCount()
```
Callback for createList().



### list_getWarningTemplates

```php
function list_getWarningTemplates($start, $items_per_page, $sort)
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### ModifyWarningTemplate

```php
function ModifyWarningTemplate()
```
Edit a warning template.



### ModerationSettings

```php
function ModerationSettings()
```
Change moderation preferences.



### ModEndSession

```php
function ModEndSession()
```
This ends a moderator session, requiring authentication to access the MCP again.



