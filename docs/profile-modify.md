---
layout: default
group: func
navtitle: Profile-Modify.php
title: ./Sources/Profile-Modify.php
count: 42
---
* auto-gen TOC:
{:toc}
### loadProfileFields

```php
function loadProfileFields(bool $force_reload = false): void
```
This defines every profile field known to man.



Type|Parameter|Description
---|---|---
`bool`|`$force_reload`|Whether to reload the data

Integration hooks
: integrate_reset_pass
: integrate_load_profile_fields

### setupProfileContext

```php
function setupProfileContext(array $fields): void
```
Setup the context for a page load!



Type|Parameter|Description
---|---|---
`array`|`$fields`|The profile fields to display. Each item should correspond to an item in the $profile_fields array generated by loadProfileFields

Integration hooks
: integrate_setup_profile_context

### saveProfileFields

```php
function saveProfileFields(): void
```
Save the profile changes.



### saveProfileChanges

```php
function saveProfileChanges(array &$profile_vars, array &$post_errors, int $memID): void
```
Save the profile changes



Type|Parameter|Description
---|---|---
`array`|`\&$profile_vars`|The items to save
`array`|`\&$post_errors`|An array of information about any errors that occurred
`int`|`$memID`|The ID of the member whose profile we're saving

### makeThemeChanges

```php
function makeThemeChanges(int $memID, int $id_theme): void
```
Make any theme changes that are sent with the profile.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the user
`int`|`$id_theme`|The ID of the theme

### makeNotificationChanges

```php
function makeNotificationChanges(int $memID): void
```
Make any notification changes that need to be made.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### makeCustomFieldChanges

```php
function makeCustomFieldChanges(int $memID, string $area, bool $sanitize = true, bool $returnErrors = false): void|array
```
Save any changes to the custom profile fields



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member
`string`|`$area`|The area of the profile these fields are in
`bool`|`$sanitize`|= true Whether or not to sanitize the data
`bool`|`$returnErrors`|Whether or not to return any error information

Integration hooks
: integrate_save_custom_profile_fields

### editBuddyIgnoreLists

```php
function editBuddyIgnoreLists(int $memID): void
```
Show all the users buddies, as well as a add/delete interface.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### editBuddies

```php
function editBuddies(int $memID): void
```
Show all the users buddies, as well as a add/delete interface.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

Integration hooks
: integrate_remove_buddy
: integrate_add_buddies
: integrate_view_buddies

### editIgnoreList

```php
function editIgnoreList(int $memID): void
```
Allows the user to view their ignore list, as well as the option to manage members on it.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### account

```php
function account(int $memID): void
```
Handles the account section of the profile



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### forumProfile

```php
function forumProfile(int $memID): void
```
Handles the main "Forum Profile" section of the profile



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### getAvatars

```php
function getAvatars(string $directory, int $level): array
```
Recursive function to retrieve server-stored avatar files



Type|Parameter|Description
---|---|---
`string`|`$directory`|The directory to look for files in
`int`|`$level`|How many levels we should go in the directory

### theme

```php
function theme(int $memID): void
```
Handles the "Look and Layout" section of the profile



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

Integration hooks
: integrate_theme_options

### notification

```php
function notification(int $memID): void
```
Display the notifications and settings for changes.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### alert_configuration

```php
function alert_configuration(int $memID, bool $defaultSettings = false): void
```
Handles configuration of alert preferences



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member
`bool`|`$defaultSettings`|If true, we are loading default options.

Integration hooks
: integrate_alert_types

### alert_markread

```php
function alert_markread(int $memID): void
```
Marks all alerts as read for the specified user



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### alert_mark

```php
function alert_mark(int $memID, array|int $toMark, int $read = 0): int
```
Marks a group of alerts as un/read



Type|Parameter|Description
---|---|---
`int`|`$memID`|The user ID.
`array`&#124;`int`|`$toMark`|The ID of a single alert or an array of IDs. The function will convert single integers to arrays for better handling.
`int`|`$read`|To mark as read or unread, 1 for read, 0 or any other value different than 1 for unread.

### alert_delete

```php
function alert_delete(int|array $toDelete, bool|int $memID = false): void|int
```
Deletes a single or a group of alerts by ID



Type|Parameter|Description
---|---|---
`int`&#124;`array`|``|The ID of a single alert to delete or an array containing the IDs of multiple alerts. The function will convert integers into an array for better handling.
`bool`&#124;`int`|`$memID`|The user ID. Used to update the user unread alerts count.

### alert_purge

```php
function alert_purge(int $memID = 0): void
```
Deletes all the alerts that a user has already read.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The user ID. Defaults to the current user's ID.

### alert_count

```php
function alert_count(int $memID, bool $unread = false): int
```
Counts how many alerts a user has - either unread or all depending on $unread
We can't use db_num_rows here, as we have to determine what boards the user can see
Possibly in future versions as database support for json is mainstream, we can simplify this.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The user ID.
`bool`|`$unread`|Whether to only count unread alerts.

### alert_notifications_topics

```php
function alert_notifications_topics(int $memID): void
```
Handles alerts related to topics and posts



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### alert_notifications_boards

```php
function alert_notifications_boards(int $memID): void
```
Handles preferences related to board-level notifications



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### list_getTopicNotificationCount

```php
function list_getTopicNotificationCount(int $memID): int
```
Determins how many topics a user has requested notifications for



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### list_getTopicNotifications

```php
function list_getTopicNotifications(int $start, int $items_per_page, string $sort, int $memID): array
```
Gets information about all the topics a user has requested notifications for. Callback for the list in alert_notifications_topics



Type|Parameter|Description
---|---|---
`int`|`$start`|Which item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to display on each page
`string`|`$sort`|A string indicating how to sort the results
`int`|`$memID`|The ID of the member

### list_getBoardNotifications

```php
function list_getBoardNotifications(int $start, int $items_per_page, string $sort, int $memID): array
```
Gets information about all the boards a user has requested notifications for. Callback for the list in alert_notifications_boards



Type|Parameter|Description
---|---|---
`int`|`$start`|Which item to start with (not used here)
`int`|`$items_per_page`|How many items to show on each page (not used here)
`string`|`$sort`|A string indicating how to sort the results
`int`|`$memID`|The ID of the member

### loadThemeOptions

```php
function loadThemeOptions(int $memID, bool $defaultSettings = false): void
```
Loads the theme options for a user



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member
`bool`|`$defaultSettings`|If true, we are loading default options.

### ignoreboards

```php
function ignoreboards(int $memID): void
```
Handles the "ignored boards" section of the profile (if enabled)



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### profileLoadLanguages

```php
function profileLoadLanguages(): bool
```
Load all the languages for the profile

.

### profileLoadGroups

```php
function profileLoadGroups(): true
```
Handles the "manage groups" section of the profile



### profileLoadSignatureData

```php
function profileLoadSignatureData(): true
```
Load key signature context data.



### profileLoadAvatarData

```php
function profileLoadAvatarData(): true
```
Load avatar context data.



### profileSaveGroups

```php
function profileSaveGroups(int &$value): true
```
Save a members group.



Type|Parameter|Description
---|---|---
`int`|`\&$value`|The ID of the (new) primary group

Integration hooks
: integrate_profile_profileSaveGroups

### profileSaveAvatarData

```php
function profileSaveAvatarData(string &$value): bool|string
```
The avatar is incredibly complicated, what with the options... and what not.



Type|Parameter|Description
---|---|---
`string`|`\&$value`|What kind of avatar we're expecting. Can be 'none', 'server_stored', 'gravatar', 'external' or 'upload'

Integration hooks
: before_profile_save_avatar
: after_profile_save_avatar

### profileValidateSignature

```php
function profileValidateSignature(string &$value): bool|string
```
Validate the signature



Type|Parameter|Description
---|---|---
`string`|`\&$value`|The new signature

### profileValidateEmail

```php
function profileValidateEmail(string $email, int $memID = 0): bool|string
```
Validate an email address.



Type|Parameter|Description
---|---|---
`string`|`$email`|The email address to validate
`int`|`$memID`|The ID of the member (used to prevent false positives from the current user)

### profileReloadUser

```php
function profileReloadUser(): void
```
Reload a user's settings.



### profileSendActivation

```php
function profileSendActivation(): void
```
Send the user a new activation email if they need to reactivate!



### groupMembership

```php
function groupMembership(int $memID): void
```
Function to allow the user to choose group membership etc.

..

Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### groupMembership2

```php
function groupMembership2(array $profile_vars, array $post_errors, int $memID): string
```
This function actually makes all the group changes



Type|Parameter|Description
---|---|---
`array`|`$profile_vars`|The profile variables
`array`|`$post_errors`|Any errors that have occurred
`int`|`$memID`|The ID of the member

### tfasetup

```php
function tfasetup(int $memID): void
```
Provides interface to setup Two Factor Auth in SMF



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### tfadisable

```php
function tfadisable(int $memID): void
```
Provides interface to disable two-factor authentication in SMF



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

