---
layout: default
group: func
navtitle: ReportToMod.php
title: ./Sources/ReportToMod.php
count: 4
---
* auto-gen TOC:
{:toc}
### ReportToModerator

```php
function ReportToModerator()
```
Report a post or profile to the moderator... ask for a comment.

Gathers data from the user to report abuse to the moderator(s).
Uses the ReportToModerator template, main sub template.
Requires the report_any permission.
Uses ReportToModerator2() if post data was sent.
Accessed through ?action=reporttm.

### ReportToModerator2

```php
function ReportToModerator2()
```
Send the emails.

Sends off emails to all the moderators.
Sends to administrators and global moderators. (1 and 2)
Called by ReportToModerator(), and thus has the same permission and setting requirements as it does.
Accessed through ?action=reporttm when posting.

### reportPost

```php
function reportPost($msg, $reason)
```
Actually reports a post using information specified from a form



Type|Parameter|Description
---|---|---
`int`|`$msg`|The ID of the post being reported
`string`|`$reason`|The reason specified for reporting the post

### reportUser

```php
function reportUser($id_member, $reason)
```
Actually reports a user's profile using information specified from a form



Type|Parameter|Description
---|---|---
`int`|`$id_member`|The ID of the member whose profile is being reported
`string`|`$reason`|The reason specified by the reporter for this report

