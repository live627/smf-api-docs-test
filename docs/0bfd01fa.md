---
layout: default
navtitle: ScheduledTasks.php
title: ./Sources/ScheduledTasks.php
count: 15
---

### AutoTask

```php
function AutoTask()
```
This function works out what to do!



### scheduled_daily_maintenance

```php
function scheduled_daily_maintenance()
```
Do some daily cleaning up.



### scheduled_daily_digest

```php
function scheduled_daily_digest()
```
Send out a daily email of all subscribed topics.



### scheduled_weekly_digest

```php
function scheduled_weekly_digest()
```
Like the daily stuff - just seven times less regular ;)



### ReduceMailQueue

```php
function ReduceMailQueue($number = false, $override_limit = false, $force_send = false)
```
Send a group of emails from the mail queue.



Type|Parameter|Description
---|---|---
```php bool&#124;int```|```php $number```|The number to send each loop through or false to use the standard limits
```php bool```|```php $override_limit```|Whether to bypass the limit
```php bool```|```php $force_send```|Whether to forcibly send the messages now (useful when using cron jobs)

### CalculateNextTrigger

```php
function CalculateNextTrigger($tasks = array(), $forceUpdate = false)
```
Calculate the next time the passed tasks should be triggered.



Type|Parameter|Description
---|---|---
```php string&#124;array```|```php $tasks```|The ID of a single task or an array of tasks
```php bool```|```php $forceUpdate```|Whether to force the tasks to run now

### next_time

```php
function next_time($regularity, $unit, $offset)
```
Simply returns a time stamp of the next instance of these time parameters.



Type|Parameter|Description
---|---|---
```php int```|```php $regularity```|The regularity
```php string```|```php $unit```|What unit are we using - 'm' for minutes, 'd' for days, 'w' for weeks or anything else for seconds
```php int```|```php $offset```|The offset

### loadEssentialThemeData

```php
function loadEssentialThemeData()
```
This loads the bare minimum data to allow us to load language files!



### scheduled_fetchSMfiles

```php
function scheduled_fetchSMfiles()
```
This retieves data (e.g. last version of SMF) from sm.org



### scheduled_birthdayemails

```php
function scheduled_birthdayemails()
```
Happy birthday!!



### scheduled_weekly_maintenance

```php
function scheduled_weekly_maintenance()
```
Weekly maintenance



### scheduled_paid_subscriptions

```php
function scheduled_paid_subscriptions()
```
Perform the standard checks on expiring/near expiring subscriptions.



### scheduled_remove_temp_attachments

```php
function scheduled_remove_temp_attachments()
```
Check for un-posted attachments is something we can do once in a while :P
This function uses opendir cycling through all the attachments



### scheduled_remove_topic_redirect

```php
function scheduled_remove_topic_redirect()
```
Check for move topic notices that have past their best by date



### scheduled_remove_old_drafts

```php
function scheduled_remove_old_drafts()
```
Check for old drafts and remove them



