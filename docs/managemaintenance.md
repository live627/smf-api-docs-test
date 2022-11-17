---
layout: default
group: func
navtitle: ManageMaintenance.php
title: ./Sources/ManageMaintenance.php
count: 28
---
* auto-gen TOC:
{:toc}
### ManageMaintenance

```php
function ManageMaintenance(): void
```
Main dispatcher, the maintenance access point.

This, as usual, checks permissions, loads language files, and forwards to the actual workers.

Integration hooks
: integrate_manage_maintenance

### MaintainDatabase

```php
function MaintainDatabase(): void
```
Supporting function for the database maintenance area.



### MaintainRoutine

```php
function MaintainRoutine(): void
```
Supporting function for the routine maintenance area.



### MaintainMembers

```php
function MaintainMembers(): void
```
Supporting function for the members maintenance area.



### MaintainTopics

```php
function MaintainTopics(): void
```
Supporting function for the topics maintenance area.



### MaintainFindFixErrors

```php
function MaintainFindFixErrors(): void
```
Find and fix all errors on the forum.



### MaintainCleanCache

```php
function MaintainCleanCache(): void
```
Wipes the whole cache.



### MaintainEmptyUnimportantLogs

```php
function MaintainEmptyUnimportantLogs(): void
```
Empties all uninmportant logs



### Destroy

```php
function Destroy(): void
```
Oh noes! I'd document this but that would give it away



### ConvertMsgBody

```php
function ConvertMsgBody(): void
```
Convert the column "body" of the table {db_prefix}messages from TEXT to MEDIUMTEXT and vice versa.

It requires the admin_forum permission.
This is needed only for MySQL.
During the conversion from MEDIUMTEXT to TEXT it check if any of the posts exceed the TEXT length and if so it aborts.
This action is linked from the maintenance screen (if it's applicable).
Accessed by ?action=admin;area=maintain;sa=database;activity=convertmsgbody.

Integration hooks
: integrate_convert_msgbody

### ConvertEntities

```php
function ConvertEntities(): void
```
Converts HTML-entities to their UTF-8 character equivalents.

This requires the admin_forum permission.
Pre-condition: UTF-8 has been set as database and global character set.

It is divided in steps of 10 seconds.
This action is linked from the maintenance screen (if applicable).
It is accessed by ?action=admin;area=maintain;sa=database;activity=convertentities.

### OptimizeTables

```php
function OptimizeTables(): void
```
Optimizes all tables in the database and lists how much was saved.

It requires the admin_forum permission.
It shows as the maintain_forum admin area.
It is accessed from ?action=admin;area=maintain;sa=database;activity=optimize.
It also updates the optimize scheduled task such that the tables are not automatically optimized again too soon.

### AdminBoardRecount

```php
function AdminBoardRecount(): void
```
Recount many forum totals that can be recounted automatically without harm.

it requires the admin_forum permission.
It shows the maintain_forum admin area.

Totals recounted:
- fixes for topics with wrong num_replies.
- updates for num_posts and num_topics of all boards.
- recounts instant_messages but not unread_messages.
- repairs messages pointing to boards with topics pointing to other boards.
- updates the last message posted in boards and children.
- updates member count, latest member, topic count, and message count.

The function redirects back to ?action=admin;area=maintain when complete.
It is accessed via ?action=admin;area=maintain;sa=database;activity=recount.

### VersionDetail

```php
function VersionDetail(): void
```
Perform a detailed version check.  A very good thing ;).

The function parses the comment headers in all files for their version information,
and outputs that for some javascript to check with simplemachines.org.
It does not connect directly with simplemachines.org, but rather expects the client to.

It requires the admin_forum permission.
Uses the view_versions admin area.
Accessed through ?action=admin;area=maintain;sa=routine;activity=version.

### MaintainReattributePosts

```php
function MaintainReattributePosts(): void
```
Re-attribute posts.



### MaintainPurgeInactiveMembers

```php
function MaintainPurgeInactiveMembers(): void
```
Removing old members. Done and out!



### MaintainRemoveOldPosts

```php
function MaintainRemoveOldPosts(): void
```
Removing old posts doesn't take much as we really pass through.



### MaintainRemoveOldDrafts

```php
function MaintainRemoveOldDrafts(): void
```
Removing old drafts



### MaintainMassMoveTopics

```php
function MaintainMassMoveTopics(): void
```
Moves topics from one board to another.



### MaintainRecountPosts

```php
function MaintainRecountPosts(): void
```
Recalculate all members post counts
it requires the admin_forum permission.

- recounts all posts for members found in the message table
- updates the members post count record in the members table
- honors the boards post count flag
- does not count posts in the recycle bin
- zeros post counts for all members with no posts in the message table
- runs as a delayed loop to avoid server overload
- uses the not_done template in Admin.template

The function redirects back to action=admin;area=maintain;sa=members when complete.
It is accessed via ?action=admin;area=maintain;sa=members;activity=recountposts

### RebuildSettingsFile

```php
function RebuildSettingsFile()
```
### list_integration_hooks

```php
function list_integration_hooks(): void
```
Generates a list of integration hooks for display
Accessed through ?action=admin;area=maintain;sa=hooks;
Allows for removal or disabling of selected hooks



### get_files_recursive

```php
function get_files_recursive(string $dirname): void
```
Gets all of the files in a directory and its children directories



Type|Parameter|Description
---|---|---
`string`|`$dirname`|The path to the directory

### get_integration_hooks_data

```php
function get_integration_hooks_data(int $start, int $per_page, string $sort, $filtered_hooks, $normalized_boarddir, $normalized_sourcedir): array
```
Callback function for the integration hooks list (list_integration_hooks)
Gets all of the hooks in the system and their status



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$per_page`|How many items to display on each page
`string`|`$sort`|A string indicating how to sort things

### get_integration_hooks

```php
function get_integration_hooks(): array
```
Parses modSettings to create integration hook array



### parse_integration_hook

```php
function parse_integration_hook(string $hook, string $rawData): array
```
Parses each hook data and returns an array.



Type|Parameter|Description
---|---|---
`string`|`$hook`|
`string`|`$rawData`|A string as it was saved to the DB.

### get_defined_functions_in_file

```php
function get_defined_functions_in_file(string $file): array
```
### fixchardb__callback

```php
function fixchardb__callback(array $matches): string
```
Converts html entities to utf8 equivalents
special db wrapper for mysql based on the limitation of mysql/mb3

Callback function for preg_replace_callback
Uses capture group 1 in the supplied array
Does basic checks to keep characters inside a viewable range.

Type|Parameter|Description
---|---|---
`array`|`$matches`|An array of matches (relevant info should be the 2nd item in the array)

