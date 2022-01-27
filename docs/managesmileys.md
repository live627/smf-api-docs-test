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
function ManageSmileys(): void
```
This is the dispatcher of smileys administration.



Integration hooks
: integrate_manage_smileys

### EditSmileySettings

```php
function EditSmileySettings(bool $return_config = false): void|array
```
Handles modifying smileys settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_modify_smiley_settings
: integrate_save_smiley_settings

### EditSmileySets

```php
function EditSmileySets(): void
```
List, add, remove, modify smileys sets.



### list_getSmileySets

```php
function list_getSmileySets(int $start, int $items_per_page, string $sort): array
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to show per page (not used here)
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSmileySets

```php
function list_getNumSmileySets(): int
```
Callback function for createList().



### AddSmiley

```php
function AddSmiley(): void
```
Add a smiley, that's right.



### EditSmileys

```php
function EditSmileys(): void
```
Add, remove, edit smileys.



### list_getSmileys

```php
function list_getSmileys(int $start, int $items_per_page, string $sort): array
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to show per page (not used here)
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSmileys

```php
function list_getNumSmileys(): int
```
Callback function for createList().



### EditSmileyOrder

```php
function EditSmileyOrder(): void
```
Allows to edit smileys order.



### InstallSmileySet

```php
function InstallSmileySet(): void
```
Install a smiley set.



### ImportSmileys

```php
function ImportSmileys(string $smileyPath, bool $create = false): void
```
A function to import new smileys from an existing directory into the database.



Type|Parameter|Description
---|---|---
`string`|`$smileyPath`|The path to the directory to import smileys from
`bool`|`$create`|Whether or not to make brand new smileys for files that don't match any existing smileys

### EditMessageIcons

```php
function EditMessageIcons(): void
```
Handles editing message icons



### list_getMessageIcons

```php
function list_getMessageIcons(int $start, int $items_per_page, string $sort): array
```
Callback function for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (not used here)
`int`|`$items_per_page`|The number of items to display per page (not used here)
`string`|`$sort`|A string indicating how to sort the items (not used here)

