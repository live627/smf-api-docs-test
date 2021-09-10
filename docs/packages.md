---
layout: default
group: func
navtitle: Packages.php
title: ./Sources/Packages.php
count: 14
---
* auto-gen TOC:
{:toc}
### Packages

```php
function Packages()
```
This is the notoriously defunct package manager..... :/.



### PackageInstallTest

```php
function PackageInstallTest()
```
Test install a package.



### PackageInstall

```php
function PackageInstall()
```
Apply another type of (avatar, language, etc.) package.



### PackageList

```php
function PackageList()
```
List the files in a package.



### ExamineFile

```php
function ExamineFile()
```
Display one of the files in a package.



### PackageRemove

```php
function PackageRemove()
```
Delete a package.



### PackageBrowse

```php
function PackageBrowse()
```
Browse a list of installed packages.



### list_getPackages

```php
function list_getPackages($start, $items_per_page, $sort, $params)
```
Get a listing of all the packages

Determines if the package is a mod, avatar, or language package and
groups it accordingly. If a package is not recognised as one of the
above, it is then put into a special group, "unknown".

Determines whether the package has been installed or not by
checking it against {@link loadInstalledPackages()}.

Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to show per page (not used here)
`string`|`$sort`|A string indicating how to sort the results
`string`|`$params`|Type of packages

### PackageOptions

```php
function PackageOptions()
```
Used when a temp FTP access is needed to package functions



### ViewOperations

```php
function ViewOperations()
```
List operations



### PackagePermissions

```php
function PackagePermissions()
```
Allow the admin to reset permissions on files.



### fetchPerms__recursive

```php
function fetchPerms__recursive($path, &$data, $level)
```
Checkes the permissions of all the areas that will be affected by the package



Type|Parameter|Description
---|---|---
`string`|`$path`|The path to the directiory to check permissions for
`array`|`$data`|An array of data about the directory
`int`|`$level`|How far deep to go

### PackagePermissionsAction

```php
function PackagePermissionsAction()
```
Actually action the permission changes they want.



### PackageFTPTest

```php
function PackageFTPTest()
```
Test an FTP connection.



