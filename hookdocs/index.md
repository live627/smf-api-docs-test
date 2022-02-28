---
layout: default
group: hooks
title: index.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_autoload

```php
call_integration_hook('integrate_autoload', array(&$classMap))
```

Type|Parameter|Description
---|---|---
`array`|`&$classMap`|desc

Called from
: [`()` in `./index.php`](../docs/index.html#)

Notes
: Since 2.1

### integrate_pre_log_stats

```php
call_integration_hook('integrate_pre_log_stats', array(&$no_stat_actions))
```

Type|Parameter|Description
---|---|---
`array`|`&$no_stat_actions`|desc

Called from
: [`smf_main()` in `./index.php`](../docs/index.html#smf_main)

Notes
: Since 2.1

### integrate_actions

```php
call_integration_hook('integrate_actions', array(&$actionArray))
```

Type|Parameter|Description
---|---|---
`array`|`&$actionArray`|desc

Called from
: [`smf_main()` in `./index.php`](../docs/index.html#smf_main)

Notes
: Since 2.1

