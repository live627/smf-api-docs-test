---
layout: default
group: func
navtitle: Help.php
title: ./Sources/Help.php
count: 3
---
* auto-gen TOC:
{:toc}
### ShowHelp

```php
function ShowHelp(): void
```
Redirect to the user help ;).

It loads information needed for the help section.
It is accessed by ?action=help.

Uses Help template and Manual language file.

### HelpIndex

```php
function HelpIndex(): void
```
The main page for the Help section



### ShowAdminHelp

```php
function ShowAdminHelp(): void
```
Show some of the more detailed help to give the admin an idea...
It shows a popup for administrative or user help.

It uses the help parameter to decide what string to display and where to get
the string from. ($helptxt or $txt?)
It is accessed via ?action=helpadmin;help=?.

Uses ManagePermissions language file, if the help starts with permissionhelp.

