---
layout: default
group: func
navtitle: ManageSearch.php
title: ./Sources/ManageSearch.php
count: 7
---
* auto-gen TOC:
{:toc}
### ManageSearch

```php
function ManageSearch()
```
Main entry point for the admin search settings screen.

It checks permissions, and it forwards to the appropriate function based on
the given sub-action.
Defaults to sub-action 'settings'.
Called by ?action=admin;area=managesearch.
Requires the admin_forum permission.

Uses ManageSearch template.
Uses Search language file.

### EditSearchSettings

```php
function EditSearchSettings($return_config = false)
```
Edit some general settings related to the search function.

Called by ?action=admin;area=managesearch;sa=settings.
Requires the admin_forum permission.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### EditWeights

```php
function EditWeights()
```
Edit the relative weight of the search factors.

Called by ?action=admin;area=managesearch;sa=weights.
Requires the admin_forum permission.

### EditSearchMethod

```php
function EditSearchMethod()
```
Edit the search method and search index used.

Calculates the size of the current search indexes in use.
Allows to create and delete a fulltext index on the messages table.
Allows to delete a custom index (that CreateMessageIndex() created).
Called by ?action=admin;area=managesearch;sa=method.
Requires the admin_forum permission.

### CreateMessageIndex

```php
function CreateMessageIndex()
```
Create a custom search index for the messages table.

Called by ?action=admin;area=managesearch;sa=createmsgindex.
Linked from the EditSearchMethod screen.
Requires the admin_forum permission.
Depending on the size of the message table, the process is divided in steps.

### loadSearchAPIs

```php
function loadSearchAPIs()
```
Get the installed Search API implementations.

This function checks for patterns in comments on top of the Search-API files!
In addition to filenames pattern.
It loads the search API classes if identified.
This function is used by EditSearchMethod to list all installed API implementations.

### detectFulltextIndex

```php
function detectFulltextIndex()
```
Checks if the message table already has a fulltext index created and returns the key name
Determines if a db is capable of creating a fulltext index



