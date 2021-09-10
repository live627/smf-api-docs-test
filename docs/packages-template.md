---
layout: default
group: func
navtitle: Packages.template.php
title: ./Themes/default/Packages.template.php
count: 17
---
* auto-gen TOC:
{:toc}
### template_main

```php
function template_main()
```
The main template



### template_view_package

```php
function template_view_package()
```
View package details when installing/uninstalling



### template_extract_package

```php
function template_extract_package()
```
Extract package contents



### template_list

```php
function template_list()
```
List files in a package



### template_examine

```php
function template_examine()
```
Examine a single file within a package



### template_browse

```php
function template_browse()
```
List all packages



### template_servers

```php
function template_servers()
```
List package servers



### template_package_confirm

```php
function template_package_confirm()
```
Confirm package operation



### template_package_list

```php
function template_package_list()
```
List packages.



### template_downloaded

```php
function template_downloaded()
```
Confirmation page showing a package was uploaded/downloaded successfully.



### template_install_options

```php
function template_install_options()
```
Installation options - FTP info and backup settings



### template_control_chmod

```php
function template_control_chmod()
```
CHMOD control form



### template_ftp_required

```php
function template_ftp_required()
```
Wrapper for the above template function showing that FTP is required



### template_view_operations

```php
function template_view_operations()
```
View operation details.



### template_file_permissions

```php
function template_file_permissions()
```
The file permissions page.



### template_permission_show_contents

```php
function template_permission_show_contents($ident, $contents, $level, $has_more = false)
```
Shows permissions for items within a directory (called from template_file_permissions)



Type|Parameter|Description
---|---|---
`string`|`$ident`|A unique ID - typically the directory name
`array`|`$contents`|An array of items within the directory
`int`|`$level`|How far to go inside the directory
`bool`|`$has_more`|Whether there are more files to display besides what's in $contents

### template_action_permissions

```php
function template_action_permissions()
```
A progress page showing what permissions changes are being applied



