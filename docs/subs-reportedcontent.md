---
layout: default
group: func
navtitle: Subs-ReportedContent.php
title: ./Sources/Subs-ReportedContent.php
count: 11
---
* auto-gen TOC:
{:toc}
### updateReport

```php
function updateReport(string $action, int $value, int|array $report_id): bool
```
Updates a report with the given parameters. Logs each action via logAction()



Type|Parameter|Description
---|---|---
`string`|`$action`|The action to perform\. Accepts "closed" and "ignore"\.
`int`|`$value`|The new value to update\.
`int` &#124; `array`|`$report_id`|The affected report\(s\)\.

### clearReportAlerts

```php
function clearReportAlerts(string $log_report, array $extra): void
```
Upon close/ignore, mark unread alerts as read.



Type|Parameter|Description
---|---|---
`string`|`$log_report`|\- what action is being taken
`array`|`$extra`|\- detailed info about the report

### countReports

```php
function countReports(int $closed = 0): int
```
Counts how many reports are in total. Used for creating pagination.



Type|Parameter|Description
---|---|---
`int`|`$closed`|1 for counting closed reports, 0 for open ones\.

### getReports

```php
function getReports(int $closed = 0): array
```
Get all possible reports the current user can see.



Type|Parameter|Description
---|---|---
`int`|`$closed`|1 for closed reports, 0 for open ones\.

### recountOpenReports

```php
function recountOpenReports(string $type): int
```
Recount all open reports. Sets a SESSION var with the updated info.



Type|Parameter|Description
---|---|---
`string`|`$type`|the type of reports to count

### getReportDetails

```php
function getReportDetails(int $report_id): array|bool
```
Gets additional information for a specific report.



Type|Parameter|Description
---|---|---
`int`|`$report_id`|The report ID to get the info from\.

### getReportComments

```php
function getReportComments(int $report_id): array|bool
```
Gets both report comments as well as any moderator comment.



Type|Parameter|Description
---|---|---
`int`|`$report_id`|The report ID to get the info from\.

### getCommentModDetails

```php
function getCommentModDetails(int $comment_id): array|bool
```
Gets specific details about a moderator comment. It also adds a permission for editing/deleting the comment,
by default only admins and the author of the comment can edit/delete it.



Type|Parameter|Description
---|---|---
`int`|`$comment_id`|The moderator comment ID to get the info from\.

### saveModComment

```php
function saveModComment(int $report_id, array $data): bool
```
Inserts a new moderator comment to the DB.



Type|Parameter|Description
---|---|---
`int`|`$report_id`|The report ID is used to fire a notification about the event\.
`array`|`$data`|a formatted array of data to be inserted\. Should be already properly sanitized\.

### editModComment

```php
function editModComment(int $comment_id, string $edited_comment): bool
```
Saves the new information whenever a moderator comment is edited.



Type|Parameter|Description
---|---|---
`int`|`$comment_id`|The edited moderator comment ID\.
`string`|`$edited_comment`|The edited moderator comment text\.

### deleteModComment

```php
function deleteModComment(int $comment_id): bool
```
Deletes a moderator comment from the DB.



Type|Parameter|Description
---|---|---
`int`|`$comment_id`|The moderator comment ID used to identify which report will be deleted\.

