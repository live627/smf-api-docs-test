---
layout: default
title: Profile-Export.php
count: 7
---

# ./Sources/Profile-Export.php

### export_profile_data

```php
function export_profile_data($uid)
```
Initiates exports a member's profile, posts, and personal messages to a file.



Type|Parameter|Name
---|---|---
int|$uid|The ID of the member whose data we're exporting.
### download_export_file

```php
function download_export_file($uid)
```
Downloads exported profile data file.



Type|Parameter|Name
---|---|---
int|$uid|The ID of the member whose data we're exporting.
### export_attachment

```php
function export_attachment($uid)
```
Allows a member to export their attachments.

Mostly just a wrapper for showAttachment() but with a few tweaks.

Type|Parameter|Name
---|---|---
int|$uid|The ID of the member whose data we're exporting.
### get_export_formats

```php
function get_export_formats()
```
Helper function that defines data export formats in a single location.



### create_export_dir

```php
function create_export_dir($fallback = '')
```
Returns the path to a secure directory for storing exported profile data.

The directory is created if it does not yet exist, and is secured using the
same method that we use to secure attachment directories. Files in this
directory can only be downloaded via the download_export_file() function.

### get_xslt_stylesheet

```php
function get_xslt_stylesheet($format, $uid)
```
Provides an XSLT stylesheet to transform an XML-based profile export file
into the desired output format.



Type|Parameter|Name
---|---|---
string|$format|The desired output format. Currently accepts 'HTML' and 'XML_XSLT'.
int|$uid|The ID of the member whose data we're exporting.
### export_load_css_js

```php
function export_load_css_js()
```
Loads and prepares CSS and JavaScript for insertion into an XSLT stylesheet.



