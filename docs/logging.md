---
layout: default
group: func
navtitle: Logging.php
title: ./Sources/Logging.php
count: 6
---
* auto-gen TOC:
{:toc}
### writeLog

```php
function writeLog($force = false)
```
Put this user in the online log.



Type|Parameter|Description
---|---|---
`bool`|`$force`|Whether to force logging the data

### logLastDatabaseError

```php
function logLastDatabaseError()
```
Logs the last database error into a file.

Attempts to use the backup file first, to store the last database error
and only update db_last_error.php if the first was successful.

### displayDebug

```php
function displayDebug()
```
This function shows the debug information tracked when $db_show_debug = true
in Settings.php



### trackStats

```php
function trackStats($stats = array())
```
Track Statistics.

Caches statistics changes, and flushes them if you pass nothing.
If '+' is used as a value, it will be incremented.
It does not actually commit the changes until the end of the page view.
It depends on the trackStats setting.

Type|Parameter|Description
---|---|---
`array`|`$stats`|An array of data

### logAction

```php
function logAction($action, array $extra = array(), $log_type = 'moderate')
```
This function logs an action to the database. It is a
thin wrapper around {@link logActions()}.



Type|Parameter|Description
---|---|---
`string`|`$action`|A code for the report; a list of such strings
can be found in Modlog.{language}.php (modlog_ac_ strings)
`array`|`$extra`|An associated array of parameters for the
item being logged. Typically this will include 'topic' for the topic's id.
`string`|`$log_type`|A string reflecting the type of log.

### logActions

```php
function logActions(array $logs)
```
Log changes to the forum, such as moderation events or administrative
changes. This behaves just like {@link logAction()} in SMF 2.0, except
that it is designed to log multiple actions at once.

SMF uses three log types:

- `user` for actions executed that aren't related to
   moderation (e.g. signature or other changes from the profile);
- `moderate` for moderation actions (e.g. topic changes);
- `admin` for administrative actions.

Type|Parameter|Description
---|---|---
`array`|`$logs`|An array of log data

