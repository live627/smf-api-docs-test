---
layout: default
group: func
navtitle: ManageLanguages.php
title: ./Sources/ManageLanguages.php
count: 10
---
* auto-gen TOC:
{:toc}
### ManageLanguages

```php
function ManageLanguages()
```
This is the main function for the languages area.

It dispatches the requests.
Loads the ManageLanguages template. (sub-actions will use it)

### AddLanguage

```php
function AddLanguage()
```
Interface for adding a new language



### list_getLanguagesList

```php
function list_getLanguagesList()
```
Gets a list of available languages from the mother ship
Will return a subset if searching, otherwise all avaialble



### DownloadLanguage

```php
function DownloadLanguage()
```
Download a language file from the Simple Machines website.

Requires a valid download ID ("did") in the URL.
Also handles installing language files.
Attempts to chmod things as needed.
Uses a standard list to display information about all the files and where they'll be put.

### ModifyLanguages

```php
function ModifyLanguages()
```
This lists all the current languages and allows editing of them.



### list_getNumLanguages

```php
function list_getNumLanguages()
```
How many languages?
Callback for the list in ManageLanguageSettings().



### list_getLanguages

```php
function list_getLanguages()
```
Fetch the actual language information.

Callback for $listOptions['get_items']['function'] in ManageLanguageSettings.
Determines which languages are available by looking for the "index.{language}.php" file.
Also figures out how many users are using a particular language.

### ModifyLanguageSettings

```php
function ModifyLanguageSettings($return_config = false)
```
Edit language related settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config_vars array (used in admin search)

### ModifyLanguage

```php
function ModifyLanguage()
```
Edit a particular set of language entries.



### cleanLangString

```php
function cleanLangString($string, $to_display = true)
```
This function cleans language entries to/from display.



Type|Parameter|Description
---|---|---
`string`|`$string`|The language string
`bool`|`$to_display`|Whether or not this is going to be displayed

