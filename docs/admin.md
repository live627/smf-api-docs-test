---
layout: default
group: func
navtitle: Admin.php
title: ./Sources/Admin.php
count: 9
---
* auto-gen TOC:
{:toc}
### AdminMain

```php
function AdminMain(): void
```
The main admin handling function.<br>
It initialises all the basic context required for the admin center.<br>
It passes execution onto the relevant admin section.<br>
If the passed section is not found it shows the admin home page.



### AdminHome

```php
function AdminHome(): void
```
The main administration section.

It prepares all the data necessary for the administration front page.
It uses the Admin template along with the admin sub template.
It requires the moderate_forum, manage_membergroups, manage_bans,
 admin_forum, manage_permissions, manage_attachments, manage_smileys,
 manage_boards, edit_news, or send_mail permission.
 It uses the index administrative area.
 It can be found by going to ?action=admin.

### DisplayAdminFile

```php
function DisplayAdminFile(): void
```
Get one of the admin information files from Simple Machines.



### AdminSearch

```php
function AdminSearch(): void
```
This function allocates out all the search stuff.



### AdminSearchInternal

```php
function AdminSearchInternal(): void
```
A complicated but relatively quick internal search.



Integration hooks
: integrate_admin_search

### AdminSearchMember

```php
function AdminSearchMember(): void
```
All this does is pass through to manage members.

{@see \ViewMembers()}

### AdminSearchOM

```php
function AdminSearchOM(): void
```
This file allows the user to search the SM online manual for a little of help.



### AdminLogs

```php
function AdminLogs(): void
```
This function decides which log to load.



Integration hooks
: integrate_manage_logs

### AdminEndSession

```php
function AdminEndSession(): void
```
This ends a admin session, requiring authentication to access the ACP again.



