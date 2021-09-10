---
layout: default
group: func
navtitle: ManageSmileys.php
title: ./Sources/ManageSmileys.php
count: 14
---
* auto-gen TOC:
{:toc}
### ManageSmileys

```php
function ManageSmileys()
```
This is the dispatcher of smileys administration.



### EditSmileySettings

```php
function EditSmileySettings($return_config = false)
```
Handles modifying smileys settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### EditSmileySets

```php
function EditSmileySets()
```
List, add, remove, modify smileys sets.



### list_getSmileySets

```php
function list_getSmileySets($start, $items_per_page, $sort)
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to show per page (not used here)
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSmileySets

```php
function list_getNumSmileySets()
```
Callback function for createList().



### AddSmiley

```php
function AddSmiley()
```
Add a smiley, that's right.



### EditSmileys

```php
function EditSmileys()
```
Add, remove, edit smileys.



### list_getSmileys

```php
function list_getSmileys($start, $items_per_page, $sort)
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to show per page (not used here)
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSmileys

```php
function list_getNumSmileys()
```
Callback function for createList().



### EditSmileyOrder

```php
function EditSmileyOrder()
```
Allows to edit smileys order.



### InstallSmileySet

```php
function InstallSmileySet()
```
Install a smiley set.



### ImportSmileys

```php
function ImportSmileys($smileyPath, $create = false)
```
A function to import new smileys from an existing directory into the database.



Type|Parameter|Description
---|---|---
`string`|`$smileyPath`|The path to the directory to import smileys from
`bool`|`$create`|Whether or not to make brand new smileys for files that don't match any existing smileys

### EditMessageIcons

```php
function EditMessageIcons()
```
Handles editing message icons



### list_getMessageIcons

```php
function list_getMessageIcons($start, $items_per_page, $sort)
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to display per page (not used here)
`string`|`$sort`|A string indicating how to sort the items (not used here)

