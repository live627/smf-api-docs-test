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
function get_single_theme(int $id, array $variables = array()): array
```
Gets a single theme's info.



Type|Parameter|Description
---|---|---
`int`|`$id`|The theme ID to get the info from\.
`string[]`|`$variables`|

Integration hooks
: integrate_get_single_theme

### get_all_themes

```php
function get_all_themes(bool $enable_only = false): void
```
Loads and returns all installed themes.

Stores all themes on $context['themes'] for easier use.

$modSettings['knownThemes'] stores themes that the user is able to select.

Type|Parameter|Description
---|---|---
`bool`|`$enable_only`|Whether to fetch only enabled themes\. Default is false\.

Integration hooks
: integrate_get_all_themes

### get_installed_themes

```php
function get_installed_themes(): void
```
Loads and returns all installed themes.

Stores all themes on $context['themes'] for easier use.

$modSettings['knownThemes'] stores themes that the user is able to select.

Integration hooks
: integrate_get_installed_themes

### get_theme_info

```php
function get_theme_info(string $path): array
```
Reads an .xml file and returns the data as an array

Removes the entire theme if the .xml file couldn't be found or read.

Type|Parameter|Description
---|---|---
`string`|`$path`|The absolute path to the xml file\.

### theme_install

```php
function theme_install(array $to_install = array()): int
```
Inserts a theme's data to the DataBase.

Ends execution with fatal_lang_error() if an error appears.

Type|Parameter|Description
---|---|---
`array`|`$to_install`|An array containing all values to be stored into the DB\.

Integration hooks
: integrate_theme_install

### remove_dir

```php
function remove_dir(string $path): bool
```
Removes a directory from the themes dir.

This is a recursive function, it will call itself if there are subdirs inside the main directory.

Type|Parameter|Description
---|---|---
`string`|`$path`|The absolute path to the directory to be removed

### remove_theme

```php
function remove_theme(int $themeID): bool
```
Removes a theme from the DB, includes all possible places where the theme might be used.



Type|Parameter|Description
---|---|---
`int`|`$themeID`|The theme ID

### get_file_listing

```php
function get_file_listing(string $path, string $relative): array
```
Generates a file listing for a given directory



Type|Parameter|Description
---|---|---
`string`|`$path`|The full path to the directory
`string`|`$relative`|The relative path \(relative to the Themes directory\)

