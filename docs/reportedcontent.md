---
layout: default
group: func
navtitle: ReportedContent.php
title: ./Sources/ReportedContent.php
count: 7
---
* auto-gen TOC:
{:toc}
### ReportedContent

```php
function ReportedContent()
```
Sets and call a function based on the given subaction. Acts as a dispatcher function.

It requires the moderate_forum permission.

Uses ModerationCenter template.
Uses ModerationCenter language file.

### ShowReports

```php
function ShowReports()
```
Shows all currently open reported posts.

Handles closing multiple reports

### ShowClosedReports

```php
function ShowClosedReports()
```
Shows all currently closed reported posts.



### ReportDetails

```php
function ReportDetails()
```
Shows detailed information about a report. such as report comments and moderator comments.

Shows a list of moderation actions for the specific report.

### HandleComment

```php
function HandleComment()
```
Creates/Deletes moderator comments.



### EditComment

```php
function EditComment()
```
Shows a textarea for editing a moderator comment.

Handles the edited comment and stores it on the DB.

### HandleReport

```php
function HandleReport()
```
Performs closing/ignoring actions for a given report.



