---
layout: default
group: func
navtitle: ManageSearchEngines.php
title: ./Sources/ManageSearchEngines.php
count: 16
---
* auto-gen TOC:
{:toc}
### SearchEngines

```php
function SearchEngines()
```
Entry point for this section.



### ManageSearchEngineSettings

```php
function ManageSearchEngineSettings($return_config = false)
```
This is really just the settings page.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the config_vars array (used for admin search)

### ViewSpiders

```php
function ViewSpiders()
```
View a list of all the spiders we know about.



### list_getSpiders

```php
function list_getSpiders($start, $items_per_page, $sort)
```
Callback function for createList()



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSpiders

```php
function list_getNumSpiders()
```
Callback function for createList()



### EditSpider

```php
function EditSpider()
```
Here we can add, and edit, spider info!



### SpiderCheck

```php
function SpiderCheck()
```
Do we think the current user is a spider?



### logSpider

```php
function logSpider()
```
Log the spider presence online.



### consolidateSpiderStats

```php
function consolidateSpiderStats()
```
This function takes any unprocessed hits and turns them into stats.



### SpiderLogs

```php
function SpiderLogs()
```
See what spiders have been up to.



### list_getSpiderLogs

```php
function list_getSpiderLogs($start, $items_per_page, $sort)
```
Callback function for createList()



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show per page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSpiderLogs

```php
function list_getNumSpiderLogs()
```
Callback function for createList()



### SpiderStats

```php
function SpiderStats()
```
Show the spider statistics.



### list_getSpiderStats

```php
function list_getSpiderStats($start, $items_per_page, $sort)
```
Callback function for createList()
Get a list of spider stats from the log_spider table



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSpiderStats

```php
function list_getNumSpiderStats()
```
Callback function for createList()
Get the number of spider stat rows from the log spider stats table



### recacheSpiderNames

```php
function recacheSpiderNames()
```
Recache spider names?



