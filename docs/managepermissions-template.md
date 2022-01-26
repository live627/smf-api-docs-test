---
layout: default
group: func
navtitle: ManagePermissions.template.php
title: ./Themes/default/ManagePermissions.template.php
count: 7
---
* auto-gen TOC:
{:toc}
### template_permission_index

```php
function template_permission_index(): void
```
The main manage permissions page



### template_by_board

```php
function template_by_board(): void
```
THe page that shows which permissions profile applies to each board



### template_edit_profiles

```php
function template_edit_profiles(): void
```
Edit permission profiles (predefined).



### template_modify_group

```php
function template_modify_group(): void
```
Modify a group's permissions



### template_modify_group_display

```php
function template_modify_group_display(string $type): void
```
The way of looking at permissions.



Type|Parameter|Description
---|---|---
`string`|`$type`|The permissions type

### template_inline_permissions

```php
function template_inline_permissions(): void
```
A form for displaying inline permissions, such as on a settings page.



### template_postmod_permissions

```php
function template_postmod_permissions(): void
```
Edit post moderation permissions.



