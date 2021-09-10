---
layout: default
group: func
navtitle: ManageMembergroups.template.php
title: ./Themes/default/ManageMembergroups.template.php
count: 6
---
* auto-gen TOC:
{:toc}
### template_main

```php
function template_main()
```
The main page listing all the groups.



### template_new_group

```php
function template_new_group()
```
Add a new membergroup.



### template_edit_group

```php
function template_edit_group()
```
Edit an existing membergroup.



### template_add_edit_group_boards_list

```php
function template_add_edit_group_boards_list($collapse = true, $form_id = 'new_group')
```
The template for determining which boards a group has access to.



Type|Parameter|Description
---|---|---
`bool`|`$collapse`|Whether to collapse the list by default

### template_group_members

```php
function template_group_members()
```
Template for viewing the members of a group.



### template_group_request_reason

```php
function template_group_request_reason()
```
Allow the moderator to enter a reason to each user being rejected.



