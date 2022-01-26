---
layout: default
group: func
navtitle: ManageAttachments.php
title: ./Sources/ManageAttachments.php
count: 21
---
* auto-gen TOC:
{:toc}
### ManageAttachments

```php
function ManageAttachments(): void
```
The main 'Attachments and Avatars' management function.

This function is the entry point for index.php?action=admin;area=manageattachments
and it calls a function based on the sub-action.
It requires the manage_attachments permission.

Uses ManageAttachments template.
Uses Admin language file.
Uses template layer 'manage_files' for showing the tab bar.

### ManageAttachmentSettings

```php
function ManageAttachmentSettings(bool $return_config = false): void|array
```
Allows to show/change attachment settings.

This is the default sub-action of the 'Attachments and Avatars' center.
Called by index.php?action=admin;area=manageattachments;sa=attachments.
Uses 'attachments' sub template.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the array of config variables (used for admin search)

### ManageAvatarSettings

```php
function ManageAvatarSettings(bool $return_config = false): void|array
```
This allows to show/change avatar settings.

Called by index.php?action=admin;area=manageattachments;sa=avatars.
Show/set permissions for permissions: 'profile_server_avatar',
	'profile_upload_avatar' and 'profile_remote_avatar'.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the config_vars array (used for admin search)

### BrowseFiles

```php
function BrowseFiles(): void
```
Show a list of attachment or avatar files.

Called by ?action=admin;area=manageattachments;sa=browse for attachments
 and ?action=admin;area=manageattachments;sa=browse;avatars for avatars.
Allows sorting by name, date, size and member.
Paginates results.

### list_getFiles

```php
function list_getFiles(int $start, int $items_per_page, string $sort, string $browse_type): array
```
Returns the list of attachments files (avatars or not), recorded
in the database, per the parameters received.



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with
`int`|`$items_per_page`|How many items to show per page
`string`|`$sort`|A string indicating how to sort results
`string`|`$browse_type`|can be one of 'avatars' or ... not. :P

### list_getNumFiles

```php
function list_getNumFiles(string $browse_type): int
```
Return the number of files of the specified type recorded in the database.

(the specified type being attachments or avatars).

Type|Parameter|Description
---|---|---
`string`|`$browse_type`|can be one of 'avatars' or not. (in which case they're attachments)

### MaintainFiles

```php
function MaintainFiles(): void
```
Show several file maintenance options.

Called by ?action=admin;area=manageattachments;sa=maintain.
Calculates file statistics (total file size, number of attachments,
number of avatars, attachment space available).

### RemoveAttachmentByAge

```php
function RemoveAttachmentByAge(): void
```
Remove attachments older than a given age.

Called from the maintenance screen by
  ?action=admin;area=manageattachments;sa=byAge.
It optionally adds a certain text to the messages the attachments
 were removed from.

### RemoveAttachmentBySize

```php
function RemoveAttachmentBySize(): void
```
Remove attachments larger than a given size.

Called from the maintenance screen by
 ?action=admin;area=manageattachments;sa=bySize.
Optionally adds a certain text to the messages the attachments were
	removed from.

### RemoveAttachment

```php
function RemoveAttachment(): void
```
Remove a selection of attachments or avatars.

Called from the browse screen as submitted form by
?action=admin;area=manageattachments;sa=remove

### RemoveAllAttachments

```php
function RemoveAllAttachments(): void
```
Removes all attachments in a single click
Called from the maintenance screen by
 ?action=admin;area=manageattachments;sa=removeall.



### removeAttachments

```php
function removeAttachments(array $condition, string $query_type = '', bool $return_affected_messages = false, bool $autoThumbRemoval = true): void|int[]
```
Removes attachments or avatars based on a given query condition.

Called by several remove avatar/attachment functions in this file.
It removes attachments based that match the $condition.
It allows query_types 'messages' and 'members', whichever is need by the
$condition parameter.
It does no permissions check.

Type|Parameter|Description
---|---|---
`array`|`$condition`|An array of conditions
`string`|`$query_type`|The query type. Can be 'messages' or 'members'
`bool`|`$return_affected_messages`|Whether to return an array with the IDs of affected messages
`bool`|`$autoThumbRemoval`|Whether to automatically remove any thumbnails associated with the removed files

### RepairAttachments

```php
function RepairAttachments(): void
```
This function should find attachments in the database that no longer exist and clear them, and fix filesize issues.



### pauseAttachmentMaintenance

```php
function pauseAttachmentMaintenance(array $to_fix, int $max_substep = 0): void
```
Function called in-between each round of attachments and avatar repairs.

Called by repairAttachments().
If repairAttachments() has more steps added, this function needs updated!

Type|Parameter|Description
---|---|---
`array`|`$to_fix`|IDs of attachments to fix
`int`|`$max_substep`|The maximum substep to reach before pausing

### ApproveAttach

```php
function ApproveAttach(): void
```
Called from a mouse click, works out what we want to do with attachments and actions it.



### ApproveAttachments

```php
function ApproveAttachments(array $attachments): void|int
```
Approve an attachment, or maybe even more - no permission check!



Type|Parameter|Description
---|---|---
`array`|`$attachments`|The IDs of the attachments to approve

### ManageAttachmentPaths

```php
function ManageAttachmentPaths(): void
```
This function lists and allows updating of multiple attachments paths.



### list_getAttachDirs

```php
function list_getAttachDirs(): array
```
Prepare the actual attachment directories to be displayed in the list.



### list_getBaseDirs

```php
function list_getBaseDirs(): void|array
```
Prepare the base directories to be displayed in a list.



### attachDirStatus

```php
function attachDirStatus(string $dir, int $expected_files): array
```
Checks the status of an attachment directory and returns an array
 of the status key, if that status key signifies an error, and
 the file count.



Type|Parameter|Description
---|---|---
`string`|`$dir`|The directory to check
`int`|`$expected_files`|How many files should be in that directory

### TransferAttachments

```php
function TransferAttachments(): void
```
Maintance function to move attachments from one directory to another



