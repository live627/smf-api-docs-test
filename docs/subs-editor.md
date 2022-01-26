---
layout: default
group: func
navtitle: Subs-Editor.php
title: ./Sources/Subs-Editor.php
count: 11
---
* auto-gen TOC:
{:toc}
### bbc_to_html

```php
function bbc_to_html(string $text, bool $compat_mode = false): string
```
As of SMF 2.1, this is unused. But it is available if any mod wants to use it.

Convert only the BBC that can be edited in HTML mode for the (old) editor.

Type|Parameter|Description
---|---|---
`string`|`$text`|The text with bbcode in it
`bool`|`$compat_mode`|Whether to actually convert the text

### html_to_bbc

```php
function html_to_bbc(string $text): string
```
Converts HTML to BBC
As of SMF 2.1, only used by ManageBoards.php (and possibly mods)



Type|Parameter|Description
---|---|---
`string`|`$text`|Text containing HTML

### fetchTagAttributes

```php
function fetchTagAttributes(string $text): array
```
Returns an array of attributes associated with a tag.



Type|Parameter|Description
---|---|---
`string`|`$text`|A tag

### legalise_bbc

```php
function legalise_bbc(string $text): string
```
Attempt to clean up illegal BBC caused by browsers like Opera which don't obey the rules



Type|Parameter|Description
---|---|---
`string`|`$text`|Text

### getMessageIcons

```php
function getMessageIcons(int $board_id): array
```
Retrieves a list of message icons.

- Based on the settings, the array will either contain a list of default
  message icons or a list of custom message icons retrieved from the database.
- The board_id is needed for the custom message icons (which can be set for
  each board individually).

Type|Parameter|Description
---|---|---
`int`|`$board_id`|The ID of the board

### create_control_richedit

```php
function create_control_richedit(array $editorOptions): void
```
Creates a box that can be used for richedit stuff like BBC, Smileys etc.



Type|Parameter|Description
---|---|---
`array`|`$editorOptions`|Various options for the editor

### create_control_verification

```php
function create_control_verification(array &$verificationOptions, bool $do_test = false): bool|array
```
Create a anti-bot verification control?



Type|Parameter|Description
---|---|---
`array`|` &$verificationOptions`|Options for the verification control
`bool`|`$do_test`|Whether to check to see if the user entered the code correctly

### AutoSuggestHandler

```php
function AutoSuggestHandler(bool $checkRegistered = null): void|bool
```
This keeps track of all registered handling functions for auto suggest functionality and passes execution to them.



Type|Parameter|Description
---|---|---
`bool`|`$checkRegistered`|If set to something other than null, checks whether the callback function is registered

### AutoSuggest_Search_Member

```php
function AutoSuggest_Search_Member(): array
```
Search for a member - by real_name or member_name by default.



### AutoSuggest_Search_MemberGroups

```php
function AutoSuggest_Search_MemberGroups(): array
```
Search for a membergroup by name



### AutoSuggest_Search_SMFVersions

```php
function AutoSuggest_Search_SMFVersions(): array
```
Provides a list of possible SMF versions to use in emulation



