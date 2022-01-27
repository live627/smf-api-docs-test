---
layout: default
group: hooks
title: Subs-Calendar.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_create_event

```php
call_integration_hook('integrate_create_event', array(&$eventOptions, &$event_columns, &$event_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`$&eventOptions`|desc
`array`|`$&event_columns`|desc
`array`|`$&event_parameters`|desc

Called from
: [`insertEvent()` in `./Sources/Subs-Calendar.php`](../docs/subs-calendar.html#insertevent)

Notes
: Since 2.1

### integrate_modify_event

```php
call_integration_hook('integrate_modify_event', array($event_id, &$eventOptions, &$event_columns, &$event_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`$event_id`|desc
`array`|`$&eventOptions`|desc
`array`|`$&event_columns`|desc
`array`|`$&event_parameters`|desc

Called from
: [`modifyEvent()` in `./Sources/Subs-Calendar.php`](../docs/subs-calendar.html#modifyevent)

Notes
: Since 2.1

### integrate_remove_event

```php
call_integration_hook('integrate_remove_event', array($event_id))
```

Type|Parameter|Description
---|---|---
`array`|`$event_id`|desc

Called from
: [`removeEvent()` in `./Sources/Subs-Calendar.php`](../docs/subs-calendar.html#removeevent)

Notes
: Since 2.1

