---
layout: default
group: func
navtitle: Subs-Membergroups.php
title: ./Sources/Subs-Membergroups.php
count: 7
---
* auto-gen TOC:
{:toc}
### deleteMembergroups

```php
function deleteMembergroups(int|array $groups): bool|string
```
Delete one of more membergroups.

Requires the manage_membergroups permission.
Returns true on success or false on failure.
Has protection against deletion of protected membergroups.
Deletes the permissions linked to the membergroup.
Takes members out of the deleted membergroups.

Type|Parameter|Description
---|---|---
`int&#124;array`|`$groups`|The ID of the group to delete or an array of IDs of groups to delete

Integration hooks
: integrate_delete_membergroups

### removeMembersFromGroups

```php
function removeMembersFromGroups(int|array $members, ?array $groups = null, bool $permissionCheckDone = false, bool $ignoreProtected = false): bool
```
Remove one or more members from one or more membergroups.

Requires the manage_membergroups permission.
Function includes a protection against removing from implicit groups.
Non-admins are not able to remove members from the admin group.

Type|Parameter|Description
---|---|---
`int&#124;array`|`$members`|The ID of a member or an array of member IDs
`null&#124;array`|``|The groups to remove the member(s) from. If null, the specified members are stripped from all their membergroups.
`bool`|`$permissionCheckDone`|Whether we've already checked permissions prior to calling this function
`bool`|`$ignoreProtected`|Whether to ignore protected groups

### addMembersToGroup

```php
function addMembersToGroup(int|array $members, int $group, string $type = 'auto', bool $permissionCheckDone = false, bool $ignoreProtected = false): bool
```
Add one or more members to a membergroup

Requires the manage_membergroups permission.
Function has protection against adding members to implicit groups.
Non-admins are not able to add members to the admin group.

Type|Parameter|Description
---|---|---
`int&#124;array`|`$members`|A single member or an array containing the IDs of members
`int`|`$group`|The group to add them to
`string`|`$type`|Specifies whether the group is added as primary or as additional group.
Supported types:
	- only_primary      - Assigns a membergroup as primary membergroup, but only
						  if a member has not yet a primary membergroup assigned,
						  unless the member is already part of the membergroup.
	- only_additional   - Assigns a membergroup to the additional membergroups,
						  unless the member is already part of the membergroup.
	- force_primary     - Assigns a membergroup as primary membergroup no matter
						  what the previous primary membergroup was.
	- auto              - Assigns a membergroup to the primary group if it's still
						  available. If not, assign it to the additional group.
`bool`|`$permissionCheckDone`|Whether we've already done a permission check
`bool`|`$ignoreProtected`|Whether to ignore protected groups

Integration hooks
: integrate_add_members_to_group

### listMembergroupMembers_Href

```php
function listMembergroupMembers_Href(array &$members, int $membergroup, int $limit = null): bool
```
Gets the members of a supplied membergroup
Returns them as a link for display



Type|Parameter|Description
---|---|---
`array`|` &$members`|The IDs of the members
`int`|`$membergroup`|The ID of the group
`int`|`$limit`|How many members to show (null for no limit)

### cache_getMembergroupList

```php
function cache_getMembergroupList(): array
```
Retrieve a list of (visible) membergroups used by the cache.



Integration hooks
: integrate_getMembergroupList

### list_getMembergroups

```php
function list_getMembergroups(int $start, int $items_per_page, string $sort, string $membergroup_type): array
```
Helper function to generate a list of membergroups for display



Type|Parameter|Description
---|---|---
`int`|`$start`|What item to start with (not used here)
`int`|`$items_per_page`|How many items to show on each page (not used here)
`string`|`$sort`|An SQL query indicating how to sort the results
`string`|`$membergroup_type`|Should be 'post_count' for post groups or anything else for regular groups

### getGroupsWithPermissions

```php
function getGroupsWithPermissions(array $group_permissions = array(), array $board_permissions = array(), int $profile_id = 1): array
```
Retrieves a list of membergroups with the given permissions.



Type|Parameter|Description
---|---|---
`array`|`$group_permissions`|
`array`|`$board_permissions`|
`int`|`$profile_id`|

