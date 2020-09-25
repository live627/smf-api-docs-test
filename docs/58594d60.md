---
layout: default
group: func
navtitle: Subs-MembersOnline.php
title: ./Sources/Subs-MembersOnline.php
count: 2
---
* auto-gen TOC:
{:toc}
### getMembersOnlineStats

```php
function getMembersOnlineStats($membersOnlineOptions)
```
Retrieve a list and several other statistics of the users currently online.

Used by the board index and SSI.
Also returns the membergroups of the users that are currently online.
(optionally) hides members that chose to hide their online presence.

Type|Parameter|Description
---|---|---
`array`|`$membersOnlineOptions`|An array of options for the list

### trackStatsUsersOnline

```php
function trackStatsUsersOnline($total_users_online)
```
Check if the number of users online is a record and store it.



Type|Parameter|Description
---|---|---
`int`|`$total_users_online`|The total number of members online

