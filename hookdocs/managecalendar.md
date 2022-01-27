---
layout: default
group: hooks
title: ManageCalendar.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_calendar

```php
call_integration_hook('integrate_manage_calendar', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageCalendar()` in `./Sources/ManageCalendar.php`](../docs/managecalendar.html#managecalendar)

Notes
: Since 2.1

### integrate_modify_calendar_settings

```php
call_integration_hook('integrate_modify_calendar_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyCalendarSettings()` in `./Sources/ManageCalendar.php`](../docs/managecalendar.html#modifycalendarsettings)

Notes
: Since 2.1

### integrate_save_calendar_settings

```php
call_integration_hook('integrate_save_calendar_settings')
```


Called from
: [`ModifyCalendarSettings()` in `./Sources/ManageCalendar.php`](../docs/managecalendar.html#modifycalendarsettings)

Notes
: Since 2.1

