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
function AdminMain()
```
The main admin handling function.<br>
It initialises all the basic context required for the admin center.<br>
It passes execution onto the relevant admin section.<br>
If the passed section is not found it shows the admin home page.



### AdminHome

```php
function AdminHome()
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
function DisplayAdminFile()
```
Get one of the admin information files from Simple Machines.



### AdminSearch

```php
function AdminSearch()
```
This function allocates out all the search stuff.



### AdminSearchInternal

```php
function AdminSearchInternal()
```
A complicated but relatively quick internal search.



### AdminSearchMember

```php
function AdminSearchMember()
```
All this does is pass through to manage members.

{@see \ViewMembers()}

### AdminSearchOM

```php
function AdminSearchOM()
```
This file allows the user to search the SM online manual for a little of help.



### AdminLogs

```php
function AdminLogs()
```
This function decides which log to load.



### AdminEndSession

```php
function AdminEndSession()
```
This ends a admin session, requiring authentication to access the ACP again.



