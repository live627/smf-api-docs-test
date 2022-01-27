---
layout: default
group: hooks
title: ManageScheduledTasks.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_scheduled_tasks

```php
call_integration_hook('integrate_manage_scheduled_tasks', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageScheduledTasks()` in `./Sources/ManageScheduledTasks.php`](../docs/managescheduledtasks.html#managescheduledtasks)

Notes
: Since 2.1

### integrate_scheduled_tasks_settings

```php
call_integration_hook('integrate_scheduled_tasks_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`TaskSettings()` in `./Sources/ManageScheduledTasks.php`](../docs/managescheduledtasks.html#tasksettings)

Notes
: Since 2.1

### integrate_save_scheduled_tasks_settings

```php
call_integration_hook('integrate_save_scheduled_tasks_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&save_vars`|desc

Called from
: [`TaskSettings()` in `./Sources/ManageScheduledTasks.php`](../docs/managescheduledtasks.html#tasksettings)

Notes
: Since 2.1

