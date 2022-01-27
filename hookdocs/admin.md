---
layout: default
group: hooks
title: Admin.php
count: 2
---
* auto-gen TOC:
{:toc}
### integrate_admin_search

```php
call_integration_hook('integrate_admin_search', array(&$language_files, &$include_files, &$settings_search))
```

Type|Parameter|Description
---|---|---
`array`|`$&language_files`|desc
`array`|`$&include_files`|desc
`array`|`$&settings_search`|desc

Called from
: [`AdminSearchInternal()` in `./Sources/Admin.php`](../docs/admin.html#adminsearchinternal)

Notes
: Since 2.1

### integrate_manage_logs

```php
call_integration_hook('integrate_manage_logs', array(&$log_functions))
```

Type|Parameter|Description
---|---|---
`array`|`$&log_functions`|desc

Called from
: [`AdminLogs()` in `./Sources/Admin.php`](../docs/admin.html#adminlogs)

Notes
: Since 2.1

