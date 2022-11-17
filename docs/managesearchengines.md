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
function SearchEngines(): void
```
Entry point for this section.



Integration hooks
: integrate_manage_search_engines

### ManageSearchEngineSettings

```php
function ManageSearchEngineSettings(bool $return_config = false): void|array
```
This is really just the settings page.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the config_vars array (used for admin search)

Integration hooks
: integrate_modify_search_engine_settings
: integrate_save_search_engine_settings

### ViewSpiders

```php
function ViewSpiders(): void
```
View a list of all the spiders we know about.



### list_getSpiders

```php
function list_getSpiders(int $start, int $items_per_page, string $sort): array
```
Callback function for createList()



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|The number of items to show per page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSpiders

```php
function list_getNumSpiders(): int
```
Callback function for createList()



### EditSpider

```php
function EditSpider(): void
```
Here we can add, and edit, spider info!



### SpiderCheck

```php
function SpiderCheck(): int
```
Do we think the current user is a spider?



### logSpider

```php
function logSpider(): void
```
Log the spider presence online.



### consolidateSpiderStats

```php
function consolidateSpiderStats(): void
```
This function takes any unprocessed hits and turns them into stats.



### SpiderLogs

```php
function SpiderLogs(): void
```
See what spiders have been up to.



### list_getSpiderLogs

```php
function list_getSpiderLogs(int $start, int $items_per_page, string $sort): array
```
Callback function for createList()



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show per page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumSpiderLogs

```php
function list_getNumSpiderLogs(): int
```
Callback function for createList()



### SpiderStats

```php
function SpiderStats(): void
```
Show the spider statistics.



### list_getSpiderStats

```php
function list_getSpiderStats(int $start, int $items_per_page, string $sort): array
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
function list_getNumSpiderStats(): int
```
Callback function for createList()
Get the number of spider stat rows from the log spider stats table



### recacheSpiderNames

```php
function recacheSpiderNames(): void
```
Recache spider names?



