---
layout: default
group: func
navtitle: PackageGet.php
title: ./Sources/PackageGet.php
count: 7
---
* auto-gen TOC:
{:toc}
### PackageGet

```php
function PackageGet(): void
```
Browse the list of package servers, add servers.

..

Integration hooks
: integrate_package_get

### PackageServers

```php
function PackageServers(): void
```
Load a list of package servers.



### PackageGBrowse

```php
function PackageGBrowse(): void
```
Browse a server's list of packages.



### PackageDownload

```php
function PackageDownload(): void
```
Download a package.



Integration hooks
: integrate_package_download

### PackageUpload

```php
function PackageUpload(): void
```
Upload a new package to the directory.



Integration hooks
: integrate_package_upload

### PackageServerAdd

```php
function PackageServerAdd(): void
```
Add a package server to the list.



### PackageServerRemove

```php
function PackageServerRemove(): void
```
Remove a server from the list.



