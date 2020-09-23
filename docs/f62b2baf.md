---
layout: default
title: ManagePermissions.php
count: 21
---

# ./Sources/ManagePermissions.php

### ModifyPermissions

```php
function ModifyPermissions()
```
Dispatches to the right function based on the given subaction.

Checks the permissions, based on the sub-action.
Called by ?action=managepermissions.

Uses ManagePermissions language file.


### PermissionIndex

```php
function PermissionIndex()
```
Sets up the permissions by membergroup index page.

Called by ?action=managepermissions
Creates an array of all the groups with the number of members and permissions.

Uses ManagePermissions language file.
Uses ManagePermissions template file.


### PermissionByBoard

```php
function PermissionByBoard()
```
Handle permissions by board... more or less. :P




### SetQuickGroups

```php
function SetQuickGroups()
```
Handles permission modification actions from the upper part of the
permission manager index.




### ModifyMembergroup

```php
function ModifyMembergroup()
```
Initializes the necessary to modify a membergroup's permissions.




### ModifyMembergroup2

```php
function ModifyMembergroup2()
```
This function actually saves modifications to a membergroup's board permissions.




### GeneralPermissionSettings

```php
function GeneralPermissionSettings($return_config = false)
```
A screen to set some general settings for permissions.



Type|Parameter|Name
---|---|---
bool|$return_config|Whether to return the $config_vars array (used for admin search)

### setPermissionLevel

```php
function setPermissionLevel($level, $group, $profile = 'null')
```
Set the permission level for a specific profile, group, or group for a profile.



Type|Parameter|Name
---|---|---
string|$level|The level ('restrict', 'standard', etc.)
int|$group|The group to set the permission for
string&#124;int|$profile|The ID of the permissions profile or 'null' if we're setting it for a group

### loadAllPermissions

```php
function loadAllPermissions()
```
Load permissions into $context['permissions'].




### init_inline_permissions

```php
function init_inline_permissions($permissions, $excluded_groups = array())
```
Initialize a form with inline permissions settings.

It loads a context variable for each permission.
This function is used by several settings screens to set specific permissions.

To exclude groups from the form for a given permission, add the group IDs as
an array to $context['excluded_permissions'][$permission]. For backwards
compatibility, it is also possible to pass group IDs in via the
$excluded_groups parameter, which will exclude the groups from the forms for
all of the permissions passed in via $permissions.

Type|Parameter|Name
---|---|---
array|$permissions|The permissions to display inline
array|$excluded_groups|The IDs of one or more groups to exclude

Uses ManagePermissions language
Uses ManagePermissions template

### theme_inline_permissions

```php
function theme_inline_permissions($permission)
```
Show a collapsible box to set a specific permission.

The function is called by templates to show a list of permissions settings.
Calls the template function template_inline_permissions().

Type|Parameter|Name
---|---|---
string|$permission|The permission to display inline

### save_inline_permissions

```php
function save_inline_permissions($permissions)
```
Save the permissions of a form containing inline permissions.



Type|Parameter|Name
---|---|---
array|$permissions|The permissions to save

### loadPermissionProfiles

```php
function loadPermissionProfiles()
```
Load permissions profiles.




### EditPermissionProfiles

```php
function EditPermissionProfiles()
```
Add/Edit/Delete profiles.




### updateChildPermissions

```php
function updateChildPermissions($parents, $profile = null)
```
This function updates the permissions of any groups based off this group.



Type|Parameter|Name
---|---|---
null&#124;array|$parents|The parent groups
null&#124;int|$profile|the ID of a permissions profile to update

### loadIllegalPermissions

```php
function loadIllegalPermissions()
```
Load permissions someone cannot grant.




### loadIllegalGuestPermissions

```php
function loadIllegalGuestPermissions()
```
Loads the permissions that can not be given to guests.

Stores the permissions in $context['non_guest_permissions'].
Also populates $context['permissions_excluded'] with the info.


### loadIllegalBBCHtmlGroups

```php
function loadIllegalBBCHtmlGroups()
```
Loads a list of membergroups who cannot be granted the bbc_html permission.

Stores the groups in $context['permissions_excluded']['bbc_html'].


### removeIllegalBBCHtmlPermission

```php
function removeIllegalBBCHtmlPermission($reload = false)
```
Removes the bbc_html permission from anyone who shouldn't have it



Type|Parameter|Name
---|---|---
bool|$reload|Before acting, refresh the list of membergroups who cannot be granted the bbc_html permission

### updateBoardManagers

```php
function updateBoardManagers()
```
Makes sure $modSettings['board_manager_groups'] is up to date.




### ModifyPostModeration

```php
function ModifyPostModeration()
```
Present a nice way of applying post moderation.




