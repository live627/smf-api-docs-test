---
layout: default
navtitle: Subs-Members.php
title: ./Sources/Subs-Members.php
count: 11
---

### deleteMembers

```php
function deleteMembers($users, $check_not_admin = false)
```
Delete one or more members.

Requires profile_remove_own or profile_remove_any permission for
respectively removing your own account or any account.
Non-admins cannot delete admins.
The function:
  - changes author of messages, topics and polls to guest authors.
  - removes all log entries concerning the deleted members, except the
error logs, ban logs and moderation logs.
  - removes these members' personal messages (only the inbox), avatars,
ban entries, theme settings, moderator positions, poll and votes.
  - updates member statistics afterwards.

Type|Parameter|Description
---|---|---
```php int&#124;array```|```php $users```|The ID of a user or an array of user IDs
```php bool```|```php $check_not_admin```|Whether to verify that the users aren't admins

### registerMember

```php
function registerMember(&$regOptions, $return_errors = false)
```
Registers a member to the forum.

Allows two types of interface: 'guest' and 'admin'. The first
includes hammering protection, the latter can perform the
registration silently.
The strings used in the options array are assumed to be escaped.
Allows to perform several checks on the input, e.g. reserved names.
The function will adjust member statistics.
If an error is detected will fatal error on all errors unless return_errors is true.

Type|Parameter|Description
---|---|---
```php array```|```php $regOptions```|An array of registration options
```php bool```|```php $return_errors```|Whether to return the errors

### isReservedName

```php
function isReservedName($name, $current_id_member = 0, $is_name = true, $fatal = true)
```
Check if a name is in the reserved words list.

(name, current member id, name/username?.)
- checks if name is a reserved name or username.
- if is_name is false, the name is assumed to be a username.
- the id_member variable is used to ignore duplicate matches with the
current member.

Type|Parameter|Description
---|---|---
```php string```|```php $name```|The name to check
```php int```|```php $current_id_member```|The ID of the current member (to avoid false positives with the current member)
```php bool```|```php $is_name```|Whether we're checking against reserved names or just usernames
```php bool```|```php $fatal```|Whether to die with a fatal error if the name is reserved

### groupsAllowedTo

```php
function groupsAllowedTo($permission, $board_id = null)
```
Retrieves a list of membergroups that are allowed to do the given
permission. (on the given board)
If board_id is not null, a board permission is assumed.

The function takes different permission settings into account.

Type|Parameter|Description
---|---|---
```php string```|```php $permission```|The permission to check
```php int```|```php $board_id```|= null If set, checks permissions for the specified board

### membersAllowedTo

```php
function membersAllowedTo($permission, $board_id = null)
```
Retrieves a list of members that have a given permission
(on a given board).

If board_id is not null, a board permission is assumed.
Takes different permission settings into account.
Takes possible moderators (on board 'board_id') into account.

Type|Parameter|Description
---|---|---
```php string```|```php $permission```|The permission to check
```php int```|```php $board_id```|If set, checks permission for that specific board

### reattributePosts

```php
function reattributePosts($memID, $email = false, $membername = false, $post_count = false)
```
This function is used to reassociate members with relevant posts.

Reattribute guest posts to a specified member.
Does not check for any permissions.
If add_to_post_count is set, the member's post count is increased.

Type|Parameter|Description
---|---|---
```php int```|```php $memID```|The ID of the original poster
```php bool&#124;string```|```php $email```|If set, should be the email of the poster
```php bool&#124;string```|```php $membername```|If set, the membername of the poster
```php bool```|```php $post_count```|Whether to adjust post counts

### BuddyListToggle

```php
function BuddyListToggle()
```
This simple function adds/removes the passed user from the current users buddy list.

Requires profile_identity_own permission.
Called by ?action=buddy;u=x;session_id=y.
Redirects to ?action=profile;u=x.

### list_getMembers

```php
function list_getMembers($start, $items_per_page, $sort, $where, $where_params = array(), $get_duplicates = false)
```
Callback for createList().



Type|Parameter|Description
---|---|---
```php int```|```php $start```|Which item to start with (for pagination purposes)
```php int```|```php $items_per_page```|How many items to show per page
```php string```|```php $sort```|An SQL query indicating how to sort the results
```php string```|```php $where```|An SQL query used to filter the results
```php array```|```php $where_params```|An array of parameters for $where
```php bool```|```php $get_duplicates```|Whether to get duplicates (used for the admin member list)

### list_getNumMembers

```php
function list_getNumMembers($where, $where_params = array())
```
Callback for createList().



Type|Parameter|Description
---|---|---
```php string```|```php $where```|An SQL query to filter the results
```php array```|```php $where_params```|An array of parameters for $where

### populateDuplicateMembers

```php
function populateDuplicateMembers(&$members)
```
Find potential duplicate registration members based on the same IP address



Type|Parameter|Description
---|---|---
```php array```|```php $members```|An array of members

### generateValidationCode

```php
function generateValidationCode()
```
Generate a random validation code.



