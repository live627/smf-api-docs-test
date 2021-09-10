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
function PlushSearch1()
```
Ask the user what they want to search for.

What it does:
- shows the screen to search forum posts (action=search)
- uses the main sub template of the Search template.
- uses the Search language file.
- requires the search_posts permission.
- decodes and loads search parameters given in the URL (if any).
- the form redirects to index.php?action=search2.

### PlushSearch2

```php
function PlushSearch2()
```
Gather the results and show them.

What it does:
- checks user input and searches the messages table for messages matching the query.
- requires the search_posts permission.
- uses the results sub template of the Search template.
- uses the Search language file.
- stores the results into the search cache.
- show the results of the search query.

### prepareSearchContext

```php
function prepareSearchContext($reset = false)
```
Callback to return messages - saves memory.

What it does:
- callback function for the results sub template.
- loads the necessary contextual data to show a search result.

Type|Parameter|Description
---|---|---
`bool`|`$reset`|Whether to reset the counter

### findSearchAPI

```php
function findSearchAPI()
```
Creates a search API and returns the object.



### searchSort

```php
function searchSort($a, $b)
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
function highlight($text, array $words)
```
Highlighting matching string



Type|Parameter|Description
---|---|---
`string`|`$text`|Text to search through
`array`|`$words`|List of keywords to search

