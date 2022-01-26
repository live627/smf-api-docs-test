---
layout: default
group: func
navtitle: Profile-Export.php
title: ./Sources/Profile-Export.php
count: 7
---
* auto-gen TOC:
{:toc}
### export_profile_data

```php
function export_profile_data(int $uid): void
```
Initiates exports a member's profile, posts, and personal messages to a file.



Type|Parameter|Description
---|---|---
`int`|`$uid`|The ID of the member whose data we're exporting.

### download_export_file

```php
function download_export_file(int $uid): void
```
Downloads exported profile data file.



Type|Parameter|Description
---|---|---
`int`|`$uid`|The ID of the member whose data we're exporting.

### export_attachment

```php
function export_attachment(int $uid): void
```
Allows a member to export their attachments.

Mostly just a wrapper for showAttachment() but with a few tweaks.

Type|Parameter|Description
---|---|---
`int`|`$uid`|The ID of the member whose data we're exporting.

### get_export_formats

```php
function get_export_formats(): array
```
Helper function that defines data export formats in a single location.



### create_export_dir

```php
function create_export_dir($fallback = ''): string|bool
```
Returns the path to a secure directory for storing exported profile data.

The directory is created if it does not yet exist, and is secured using the
same method that we use to secure attachment directories. Files in this
directory can only be downloaded via the download_export_file() function.

### get_xslt_stylesheet

```php
function get_xslt_stylesheet(string $format, int $uid): array
```
Provides an XSLT stylesheet to transform an XML-based profile export file
into the desired output format.



Type|Parameter|Description
---|---|---
`string`|`$format`|The desired output format. Currently accepts 'HTML' and 'XML_XSLT'.
`int`|`$uid`|The ID of the member whose data we're exporting.

### export_load_css_js

```php
function export_load_css_js(): void
```
Loads and prepares CSS and JavaScript for insertion into an XSLT stylesheet.



