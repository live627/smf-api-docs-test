---
layout: default
group: func
navtitle: ManageMembergroups.php
title: ./Sources/ManageMembergroups.php
count: 6
---
* auto-gen TOC:
{:toc}
### ModifyMembergroups

```php
function ModifyMembergroups(): void
```
Main dispatcher, the entrance point for all 'Manage Membergroup' actions.

It forwards to a function based on the given subaction, default being subaction 'index', or, without manage_membergroup
permissions, then 'settings'.
Called by ?action=admin;area=membergroups.
Requires the manage_membergroups or the admin_forum permission.

Uses ManageMembergroups template.
Uses ManageMembers language file.

### MembergroupIndex

```php
function MembergroupIndex(): void
```
Shows an overview of the current membergroups.

Called by ?action=admin;area=membergroups.
Requires the manage_membergroups permission.
Splits the membergroups in regular ones and post count based groups.
It also counts the number of members part of each membergroup.

Uses ManageMembergroups template, main.

### AddMembergroup

```php
function AddMembergroup(): void
```
This function handles adding a membergroup and setting some initial properties.

Called by ?action=admin;area=membergroups;sa=add.
It requires the manage_membergroups permission.
Allows to use a predefined permission profile or copy one from another group.
Redirects to action=admin;area=membergroups;sa=edit;group=x.

### DeleteMembergroup

```php
function DeleteMembergroup(): void
```
Deleting a membergroup by URL (not implemented).

Called by ?action=admin;area=membergroups;sa=delete;group=x;session_var=y.
Requires the manage_membergroups permission.
Redirects to ?action=admin;area=membergroups.

### EditMembergroup

```php
function EditMembergroup(): void
```
Editing a membergroup.

Screen to edit a specific membergroup.
Called by ?action=admin;area=membergroups;sa=edit;group=x.
It requires the manage_membergroups permission.
Also handles the delete button of the edit form.
Redirects to ?action=admin;area=membergroups.

### ModifyMembergroupsettings

```php
function ModifyMembergroupsettings(): void
```
Set some general membergroup settings and permissions.

Called by ?action=admin;area=membergroups;sa=settings
Requires the admin_forum permission (and manage_permissions for changing permissions)
Redirects to itself.

