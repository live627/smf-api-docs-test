---
layout: default
group: func
navtitle: ModerationCenter.php
title: ./Sources/ModerationCenter.php
count: 24
---
* auto-gen TOC:
{:toc}
### ModerationMain

```php
function ModerationMain(bool $dont_call = false): void
```
Entry point for the moderation center.



Type|Parameter|Description
---|---|---
`bool`|`$dont_call`|If true, doesn't call the function for the appropriate mod area

### ModerationHome

```php
function ModerationHome(): void
```
This function basically is the home page of the moderation center.



Integration hooks
: integrate_mod_centre_blocks

### ModBlockWatchedUsers

```php
function ModBlockWatchedUsers(): void
```
Show a list of the most active watched users.



### ModBlockNotes

```php
function ModBlockNotes(): void
```
Show an area for the moderator to type into.



### ModBlockReportedPosts

```php
function ModBlockReportedPosts(): void
```
Show a list of the most recent reported posts.



### ModBlockGroupRequests

```php
function ModBlockGroupRequests(): void
```
Show a list of all the group requests they can see.



### ModBlockReportedMembers

```php
function ModBlockReportedMembers(): void
```
Show a list of the most recent reported posts.



### ModerateGroups

```php
function ModerateGroups(): void
```
Act as an entrace for all group related activity.



### ShowNotice

```php
function ShowNotice(): void
```
Show a notice sent to a user.



### ViewWatchedUsers

```php
function ViewWatchedUsers(): void
```
View watched users.



### list_getWatchedUserCount

```php
function list_getWatchedUserCount(string $approve_query): int
```
Callback for createList().



Type|Parameter|Description
---|---|---
`string`|`$approve_query`|Not used here

### list_getWatchedUsers

```php
function list_getWatchedUsers(int $start, int $items_per_page, string $sort, string $approve_query, string $dummy): void
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with \(for pagination purposes\)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort things
`string`|`$approve_query`|A query for approving things\. Not used here\.
`string`|`$dummy`|Not used here\.

### list_getWatchedUserPostsCount

```php
function list_getWatchedUserPostsCount(string $approve_query): int
```
Callback for createList().



Type|Parameter|Description
---|---|---
`string`|`$approve_query`|A query to pull only approved items

### list_getWatchedUserPosts

```php
function list_getWatchedUserPosts(int $start, int $items_per_page, string $sort, string $approve_query, array $delete_boards): array
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with \(for pagination purposes\)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results \(not used here\)
`string`|`$approve_query`|A query to only pull approved items
`int[]`|`$delete_boards`|An array containing the IDs of boards we can delete posts in

### ViewWarnings

```php
function ViewWarnings(): void
```
Entry point for viewing warning related stuff.



Integration hooks
: integrate_warning_log_actions

### ViewWarningLog

```php
function ViewWarningLog(): void
```
Simply put, look at the warning log!



### list_getWarningCount

```php
function list_getWarningCount(): int
```
Callback for createList().



### list_getWarnings

```php
function list_getWarnings(int $start, int $items_per_page, string $sort): array
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with \(for pagination purposes\)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### ViewWarningTemplates

```php
function ViewWarningTemplates(): void
```
Load all the warning templates.



### list_getWarningTemplateCount

```php
function list_getWarningTemplateCount(): int
```
Callback for createList().



### list_getWarningTemplates

```php
function list_getWarningTemplates(int $start, int $items_per_page, string $sort): array
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with \(for pagination purposes\)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### ModifyWarningTemplate

```php
function ModifyWarningTemplate(): void
```
Edit a warning template.



### ModerationSettings

```php
function ModerationSettings(): void
```
Change moderation preferences.



### ModEndSession

```php
function ModEndSession(): void
```
This ends a moderator session, requiring authentication to access the MCP again.



