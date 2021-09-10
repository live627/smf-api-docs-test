---
layout: default
group: func
navtitle: Stats.php
title: ./Sources/Stats.php
count: 3
---
* auto-gen TOC:
{:toc}
### DisplayStats

```php
function DisplayStats()
```
Display some useful/interesting board statistics.

gets all the statistics in order and puts them in.
uses the Stats template and language file. (and main sub template.)
requires the view_stats permission.
accessed from ?action=stats.

### getDailyStats

```php
function getDailyStats($condition_string, $condition_parameters = array())
```
Loads the statistics on a daily basis in $context.

called by DisplayStats().

Type|Parameter|Description
---|---|---
`string`|`$condition_string`|An SQL condition string
`array`|`$condition_parameters`|Parameters for $condition_string

### SMStats

```php
function SMStats()
```
This is the function which returns stats to simplemachines.org IF enabled!
called by simplemachines.org.

only returns anything if stats was enabled during installation.
can also be accessed by the admin, to show what stats sm.org collects.
does not return any data directly to sm.org, instead starts a new request for security.

