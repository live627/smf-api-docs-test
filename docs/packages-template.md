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
function template_main(): void
```
The main template



### template_view_package

```php
function template_view_package(): void
```
View package details when installing/uninstalling



### template_extract_package

```php
function template_extract_package(): void
```
Extract package contents



### template_list

```php
function template_list(): void
```
List files in a package



### template_examine

```php
function template_examine(): void
```
Examine a single file within a package



### template_browse

```php
function template_browse(): void
```
List all packages



### template_servers

```php
function template_servers(): void
```
List package servers



### template_package_confirm

```php
function template_package_confirm(): void
```
Confirm package operation



### template_package_list

```php
function template_package_list(): void
```
List packages.



### template_downloaded

```php
function template_downloaded(): void
```
Confirmation page showing a package was uploaded/downloaded successfully.



### template_install_options

```php
function template_install_options(): void
```
Installation options - FTP info and backup settings



### template_control_chmod

```php
function template_control_chmod(): bool
```
CHMOD control form



### template_ftp_required

```php
function template_ftp_required(): void
```
Wrapper for the above template function showing that FTP is required



### template_view_operations

```php
function template_view_operations(): void
```
View operation details.



### template_file_permissions

```php
function template_file_permissions(): void
```
The file permissions page.



### template_permission_show_contents

```php
function template_permission_show_contents(string $ident, array $contents, int $level, bool $has_more = false): void
```
Shows permissions for items within a directory (called from template_file_permissions)



Type|Parameter|Description
---|---|---
`string`|`$ident`|A unique ID \- typically the directory name
`array`|`$contents`|An array of items within the directory
`int`|`$level`|How far to go inside the directory
`bool`|`$has_more`|Whether there are more files to display besides what's in $contents

### template_action_permissions

```php
function template_action_permissions(): void
```
A progress page showing what permissions changes are being applied



