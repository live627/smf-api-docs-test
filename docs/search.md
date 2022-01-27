---
layout: default
group: func
navtitle: Search.php
title: ./Sources/Search.php
count: 6
---
* auto-gen TOC:
{:toc}
### PlushSearch1

```php
function PlushSearch1(): void
```
Ask the user what they want to search for.

What it does:
- shows the screen to search forum posts (action=search)
- uses the main sub template of the Search template.
- uses the Search language file.
- requires the search_posts permission.
- decodes and loads search parameters given in the URL (if any).
- the form redirects to index.php?action=search2.

Integration hooks
: integrate_search

### PlushSearch2

```php
function PlushSearch2(): void
```
Gather the results and show them.

What it does:
- checks user input and searches the messages table for messages matching the query.
- requires the search_posts permission.
- uses the results sub template of the Search template.
- uses the Search language file.
- stores the results into the search cache.
- show the results of the search query.

Integration hooks
: integrate_search_weights
: integrate_search_sort_columns
: integrate_search_params
: integrate_search_blacklisted_words
: integrate_search_errors
: integrate_subject_only_search_query
: integrate_subject_search_query
: integrate_main_search_query
: integrate_search_message_list

### prepareSearchContext

```php
function prepareSearchContext(bool $reset = false): array
```
Callback to return messages - saves memory.

What it does:
- callback function for the results sub template.
- loads the necessary contextual data to show a search result.

Type|Parameter|Description
---|---|---
`bool`|`$reset`|Whether to reset the counter

Integration hooks
: integrate_quick_mod_actions_search
: integrate_search_message_context

### findSearchAPI

```php
function findSearchAPI(): \search_api_interface
```
Creates a search API and returns the object.



### searchSort

```php
function searchSort(string $a, string $b): int
```
This function compares the length of two strings plus a little.

What it does:
- callback function for usort used to sort the fulltext results.
- passes sorting duty to the current API.

Type|Parameter|Description
---|---|---
`string`|`$a`|
`string`|`$b`|

### highlight

```php
function highlight(string $text, array $words): string
```
Highlighting matching string



Type|Parameter|Description
---|---|---
`string`|`$text`|Text to search through
`array`|`$words`|List of keywords to search

