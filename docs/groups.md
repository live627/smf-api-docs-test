---
layout: default
group: func
navtitle: Groups.php
title: ./Sources/Groups.php
count: 6
---
* auto-gen TOC:
{:toc}
### Groups

```php
function Groups(): void
```
Entry point function, permission checks, admin bars, etc.

It allows moderators and users to access the group showing functions.
It handles permission checks, and puts the moderation bar on as required.

### GroupList

```php
function GroupList(): void
```
This very simply lists the groups, nothing snazy.



### MembergroupMembers

```php
function MembergroupMembers(): void
```
Display members of a group, and allow adding of members to a group. Silly function name though ;)
It can be called from ManageMembergroups if it needs templating within the admin environment.

It shows a list of members that are part of a given membergroup.
It is called by ?action=moderate;area=viewgroups;sa=members;group=x
It requires the manage_membergroups permission.
It allows to add and remove members from the selected membergroup.
It allows sorting on several columns.
It redirects to itself.

### GroupRequests

```php
function GroupRequests(): void
```
Show and manage all group requests.



### list_getGroupRequestCount

```php
function list_getGroupRequestCount(string $where, array $where_parameters): int
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`string`|`$where`|The WHERE clause for the query
`array`|`$where_parameters`|The parameters for the WHERE clause

### list_getGroupRequests

```php
function list_getGroupRequests(int $start, int $items_per_page, string $sort, string $where, string $where_parameters): array
```
Callback function for createList()



Type|Parameter|Description
---|---|---
`int`|`$start`|The result to start with
`int`|`$items_per_page`|The number of items per page
`string`|`$sort`|An SQL sort expression (column/direction)
`string`|`$where`|Data for the WHERE clause
`string`|`$where_parameters`|Parameter values to be inserted into the WHERE clause

