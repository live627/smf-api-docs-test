---
layout: default
group: func
navtitle: Subs-Themes.php
title: ./Sources/Subs-Themes.php
count: 8
---
* auto-gen TOC:
{:toc}
### get_single_theme

```php
function get_single_theme($id, array $variables = array())
```
Gets a single theme's info.



Type|Parameter|Description
---|---|---
`int`|`$id`|The theme ID to get the info from.
`string[]`|`$variables`|

### get_all_themes

```php
function get_all_themes($enable_only = false)
```
Loads and returns all installed themes.

Stores all themes on $context['themes'] for easier use.

$modSettings['knownThemes'] stores themes that the user is able to select.

Type|Parameter|Description
---|---|---
`bool`|`$enable_only`|Whether to fetch only enabled themes. Default is false.

### get_installed_themes

```php
function get_installed_themes()
```
Loads and returns all installed themes.

Stores all themes on $context['themes'] for easier use.

$modSettings['knownThemes'] stores themes that the user is able to select.

### get_theme_info

```php
function get_theme_info($path)
```
Reads an .xml file and returns the data as an array

Removes the entire theme if the .xml file couldn't be found or read.

Type|Parameter|Description
---|---|---
`string`|`$path`|The absolute path to the xml file.

### theme_install

```php
function theme_install($to_install = array())
```
Inserts a theme's data to the DataBase.

Ends execution with fatal_lang_error() if an error appears.

Type|Parameter|Description
---|---|---
`array`|`$to_install`|An array containing all values to be stored into the DB.

### remove_dir

```php
function remove_dir($path)
```
Removes a directory from the themes dir.

This is a recursive function, it will call itself if there are subdirs inside the main directory.

Type|Parameter|Description
---|---|---
`string`|`$path`|The absolute path to the directory to be removed

### remove_theme

```php
function remove_theme($themeID)
```
Removes a theme from the DB, includes all possible places where the theme might be used.



Type|Parameter|Description
---|---|---
`int`|`$themeID`|The theme ID

### get_file_listing

```php
function get_file_listing($path, $relative)
```
Generates a file listing for a given directory



Type|Parameter|Description
---|---|---
`string`|`$path`|The full path to the directory
`string`|`$relative`|The relative path (relative to the Themes directory)

