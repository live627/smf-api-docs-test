---
layout: default
group: func
navtitle: ScheduledTasks.php
title: ./Sources/ScheduledTasks.php
count: 16
---
* auto-gen TOC:
{:toc}
### AutoTask

```php
function AutoTask(): void
```
This function works out what to do!



### scheduled_daily_maintenance

```php
function scheduled_daily_maintenance(): void
```
Do some daily cleaning up.



Integration hooks
: integrate_daily_maintenance

### scheduled_daily_digest

```php
function scheduled_daily_digest(): void
```
Send out a daily email of all subscribed topics.



Integration hooks
: integrate_daily_digest_lang
: integrate_daily_digest_email

### scheduled_weekly_digest

```php
function scheduled_weekly_digest(): void
```
Like the daily stuff - just seven times less regular ;)



### ReduceMailQueue

```php
function ReduceMailQueue(bool|int $number = false, bool $override_limit = false, bool $force_send = false): bool
```
Send a group of emails from the mail queue.



Type|Parameter|Description
---|---|---
`bool` &#124; `int`|`$number`|The number to send each loop through or false to use the standard limits
`bool`|`$override_limit`|Whether to bypass the limit
`bool`|`$force_send`|Whether to forcibly send the messages now \(useful when using cron jobs\)

### CalculateNextTrigger

```php
function CalculateNextTrigger(string|array $tasks = array(), bool $forceUpdate = false): void
```
Calculate the next time the passed tasks should be triggered.



Type|Parameter|Description
---|---|---
`string` &#124; `array`|`$tasks`|The ID of a single task or an array of tasks
`bool`|`$forceUpdate`|Whether to force the tasks to run now

### next_time

```php
function next_time(int $regularity, string $unit, int $offset): int
```
Simply returns a time stamp of the next instance of these time parameters.



Type|Parameter|Description
---|---|---
`int`|`$regularity`|The regularity
`string`|`$unit`|What unit are we using \- 'm' for minutes, 'd' for days, 'w' for weeks or anything else for seconds
`int`|`$offset`|The offset

### loadEssentialThemeData

```php
function loadEssentialThemeData(): void
```
This loads the bare minimum data to allow us to load language files!



### scheduled_fetchSMfiles

```php
function scheduled_fetchSMfiles(): void
```
This retieves data (e.g. last version of SMF) from sm.org



### scheduled_birthdayemails

```php
function scheduled_birthdayemails(): void
```
Happy birthday!!



### scheduled_weekly_maintenance

```php
function scheduled_weekly_maintenance(): void
```
Weekly maintenance



Integration hooks
: integrate_weekly_maintenance

### scheduled_paid_subscriptions

```php
function scheduled_paid_subscriptions(): void
```
Perform the standard checks on expiring/near expiring subscriptions.



### scheduled_remove_temp_attachments

```php
function scheduled_remove_temp_attachments(): void
```
Check for un-posted attachments is something we can do once in a while :P
This function uses opendir cycling through all the attachments



### scheduled_remove_topic_redirect

```php
function scheduled_remove_topic_redirect(): void
```
Check for move topic notices that have past their best by date



### scheduled_remove_old_drafts

```php
function scheduled_remove_old_drafts(): void
```
Check for old drafts and remove them



### scheduled_prune_log_topics

```php
function scheduled_prune_log_topics(): void
```
Prune log_topics, log_boards & log_mark_boards_read.

For users who haven't been active in a long time, purge these records.
For users who haven't been active in a shorter time, mark boards as read,
pruning log_topics.

