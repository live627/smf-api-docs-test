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
function Packages(): void
```
This is the notoriously defunct package manager..... :/.



### PackageInstallTest

```php
function PackageInstallTest(): void
```
Test install a package.



### PackageInstall

```php
function PackageInstall(): void
```
Apply another type of (avatar, language, etc.) package.



### PackageList

```php
function PackageList(): void
```
List the files in a package.



### ExamineFile

```php
function ExamineFile(): void
```
Display one of the files in a package.



### PackageRemove

```php
function PackageRemove(): void
```
Delete a package.



### PackageBrowse

```php
function PackageBrowse(): void
```
Browse a list of installed packages.



### list_getPackages

```php
function list_getPackages(int $start, int $items_per_page, string $sort, string $params): array
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
function PackageOptions(): void
```
Used when a temp FTP access is needed to package functions



### ViewOperations

```php
function ViewOperations(): void
```
List operations



### PackagePermissions

```php
function PackagePermissions(): void
```
Allow the admin to reset permissions on files.



### fetchPerms__recursive

```php
function fetchPerms__recursive(string $path, array &$data, int $level): void
```
Checkes the permissions of all the areas that will be affected by the package



Type|Parameter|Description
---|---|---
`string`|`$path`|The path to the directiory to check permissions for
`array`|`$data`|An array of data about the directory
`int`|`$level`|How far deep to go

### PackagePermissionsAction

```php
function PackagePermissionsAction(): void
```
Actually action the permission changes they want.



### PackageFTPTest

```php
function PackageFTPTest(): void
```
Test an FTP connection.



