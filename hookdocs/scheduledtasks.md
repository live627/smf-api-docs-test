---
layout: default
group: hooks
title: ScheduledTasks.php
count: 4
---
* auto-gen TOC:
{:toc}

## ScheduledTasks.php
### integrate_daily_maintenance

```php
call_integration_hook('integrate_daily_maintenance')
```


Called from
: [`scheduled_daily_maintenance()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_daily_maintenance)

Notes
: Since 2.1

### integrate_daily_digest_lang

```php
call_integration_hook('integrate_daily_digest_lang', array(&$langtxt, $lang))
```

Type|Parameter|Description
---|---|---
`array`|`&$langtxt`|desc
`array`|`$lang`|desc

Called from
: [`scheduled_daily_digest()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_daily_digest)

Notes
: Since 2.1

### integrate_daily_digest_email

```php
call_integration_hook('integrate_daily_digest_email', array(&$email, $types, $notify_types, $langtxt))
```

Type|Parameter|Description
---|---|---
`array`|`&$email`|desc
`array`|`$types`|desc
`array`|`$notify_types`|desc
`array`|`$langtxt`|desc

Called from
: [`scheduled_daily_digest()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_daily_digest)

Notes
: Since 2.1

### integrate_weekly_maintenance

```php
call_integration_hook('integrate_weekly_maintenance')
```


Called from
: [`scheduled_weekly_maintenance()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_weekly_maintenance)

Notes
: Since 2.1

