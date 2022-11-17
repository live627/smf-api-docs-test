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
function ManageLanguages(): void
```
This is the main function for the languages area.

It dispatches the requests.
Loads the ManageLanguages template. (sub-actions will use it)

Integration hooks
: integrate_manage_languages

### AddLanguage

```php
function AddLanguage(): void
```
Interface for adding a new language



### list_getLanguagesList

```php
function list_getLanguagesList(): array
```
Gets a list of available languages from the mother ship
Will return a subset if searching, otherwise all avaialble



### DownloadLanguage

```php
function DownloadLanguage(): void
```
Download a language file from the Simple Machines website.

Requires a valid download ID ("did") in the URL.
Also handles installing language files.
Attempts to chmod things as needed.
Uses a standard list to display information about all the files and where they'll be put.

### ModifyLanguages

```php
function ModifyLanguages(): void
```
This lists all the current languages and allows editing of them.



### list_getNumLanguages

```php
function list_getNumLanguages(): int
```
How many languages?
Callback for the list in ManageLanguageSettings().



### list_getLanguages

```php
function list_getLanguages(): array
```
Fetch the actual language information.

Callback for $listOptions['get_items']['function'] in ManageLanguageSettings.
Determines which languages are available by looking for the "index.{language}.php" file.
Also figures out how many users are using a particular language.

### ModifyLanguageSettings

```php
function ModifyLanguageSettings(bool $return_config = false): void|array
```
Edit language related settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config\_vars array \(used in admin search\)

Integration hooks
: integrate_language_settings
: integrate_save_language_settings

### ModifyLanguage

```php
function ModifyLanguage(): void
```
Edit a particular set of language entries.



Integration hooks
: integrate_modifylanguages
: integrate_language_edit_helptext

### cleanLangString

```php
function cleanLangString(string $string, bool $to_display = true): string
```
This function cleans language entries to/from display.



Type|Parameter|Description
---|---|---
`string`|`$string`|The language string
`bool`|`$to_display`|Whether or not this is going to be displayed

