---
layout: default
group: hooks
title: Load
count: 21
---
{:toc}
## Load.php
### integrate_load_average

```php
call_integration_hook('integrate_load_average', array($modSettings['load_average']))
```

Type|Parameter|Description
---|---|---
`array`|`$load_average`|desc

Called from
: [`reloadSettings()` in `./Sources/Load.php`](../docs/load.html#reloadsettings)

Notes
: Since 2.1

### integrate_pre_load

```php
call_integration_hook('integrate_pre_load')
```


Called from
: [`reloadSettings()` in `./Sources/Load.php`](../docs/load.html#reloadsettings)

Notes
: Since 2.1

### integrate_verify_user

```php
call_integration_hook('integrate_verify_user')
```


Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_force_tfasetup

```php
call_integration_hook('integrate_force_tfasetup', array(&$force_tfasetup))
```

Type|Parameter|Description
---|---|---
`array`|`&$force_tfasetup`|desc

Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_verify_tfa

```php
call_integration_hook('integrate_verify_tfa', array($id_member, $user_settings))
```

Type|Parameter|Description
---|---|---
`array`|`$id_member`|desc
`array`|`$user_settings`|desc

Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_user_info

```php
call_integration_hook('integrate_user_info')
```


Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_load_min_user_settings_columns

```php
call_integration_hook('integrate_load_min_user_settings_columns', array(&$columns_to_load))
```

Type|Parameter|Description
---|---|---
`array`|`&$columns_to_load`|desc

Called from
: [`loadMinUserInfo()` in `./Sources/Load.php`](../docs/load.html#loadminuserinfo)

Notes
: Since 2.1

### integrate_load_min_user_settings

```php
call_integration_hook('integrate_load_min_user_settings', array(&$user_info_min))
```

Type|Parameter|Description
---|---|---
`array`|`&$user_info_min`|desc

Called from
: [`loadMinUserInfo()` in `./Sources/Load.php`](../docs/load.html#loadminuserinfo)

Notes
: Since 2.1

### integrate_load_board

```php
call_integration_hook('integrate_load_board', array(&$custom_column_selects, &$custom_column_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$custom_column_selects`|desc
`array`|`&$custom_column_parameters`|desc

Called from
: [`loadBoard()` in `./Sources/Load.php`](../docs/load.html#loadboard)

Notes
: Since 2.1

### integrate_board_info

```php
call_integration_hook('integrate_board_info', array(&$board_info, $row))
```

Type|Parameter|Description
---|---|---
`array`|`&$board_info`|desc
`array`|`$row`|desc

Called from
: [`loadBoard()` in `./Sources/Load.php`](../docs/load.html#loadboard)

Notes
: Since 2.1

### integrate_load_member_data

```php
call_integration_hook('integrate_load_member_data', array(&$select_columns, &$select_tables, &$set))
```

Type|Parameter|Description
---|---|---
`array`|`&$select_columns`|desc
`array`|`&$select_tables`|desc
`array`|`&$set`|desc

Called from
: [`loadMemberData()` in `./Sources/Load.php`](../docs/load.html#loadmemberdata)

Notes
: Since 2.1

### integrate_member_context

```php
call_integration_hook('integrate_member_context', array(&$memberContext[$user], $user, $display_custom_fields))
```

Type|Parameter|Description
---|---|---
`array`|`&$user`|desc
`array`|`$user`|desc
`array`|`$display_custom_fields`|desc

Called from
: [`loadMemberContext()` in `./Sources/Load.php`](../docs/load.html#loadmembercontext)

Notes
: Since 2.1

### integrate_pre_load_theme

```php
call_integration_hook('integrate_pre_load_theme', array(&$id_theme))
```

Type|Parameter|Description
---|---|---
`array`|`&$id_theme`|desc

Called from
: [`loadTheme()` in `./Sources/Load.php`](../docs/load.html#loadtheme)

Notes
: Since 2.1

### integrate_simple_actions

```php
call_integration_hook('integrate_simple_actions', array(&$simpleActions, &$simpleAreas, &$simpleSubActions, &$extraParams, &$xmlActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$simpleActions`|desc
`array`|`&$simpleAreas`|desc
`array`|`&$simpleSubActions`|desc
`array`|`&$extraParams`|desc
`array`|`&$xmlActions`|desc

Called from
: [`loadTheme()` in `./Sources/Load.php`](../docs/load.html#loadtheme)

Notes
: Since 2.1

### integrate_load_theme

```php
call_integration_hook('integrate_load_theme')
```


Called from
: [`triggerCron()` in `./Sources/Load.php`](../docs/load.html#triggercron)

Notes
: Since 2.1

### pre_cache_quick_get

```php
call_integration_hook('pre_cache_quick_get', array(&$key, &$file, &$function, &$params, &$level))
```

Type|Parameter|Description
---|---|---
`array`|`&$key`|desc
`array`|`&$file`|desc
`array`|`&$function`|desc
`array`|`&$params`|desc
`array`|`&$level`|desc

Called from
: [`cache_quick_get()` in `./Sources/Load.php`](../docs/load.html#cache_quick_get)

Notes
: Since 2.1

### post_cache_quick_get

```php
call_integration_hook('post_cache_quick_get', array(&$cache_block))
```

Type|Parameter|Description
---|---|---
`array`|`&$cache_block`|desc

Called from
: [`cache_quick_get()` in `./Sources/Load.php`](../docs/load.html#cache_quick_get)

Notes
: Since 2.1

### cache_put_data

```php
call_integration_hook('cache_put_data', array(&$key, &$value, &$ttl))
```

Type|Parameter|Description
---|---|---
`array`|`&$key`|desc
`array`|`&$value`|desc
`array`|`&$ttl`|desc

Called from
: [`cache_put_data()` in `./Sources/Load.php`](../docs/load.html#cache_put_data)

Notes
: Since 2.1

### cache_get_data

```php
call_integration_hook('cache_get_data', array(&$key, &$ttl, &$value))
```

Type|Parameter|Description
---|---|---
`array`|`&$key`|desc
`array`|`&$ttl`|desc
`array`|`&$value`|desc

Called from
: [`cache_get_data()` in `./Sources/Load.php`](../docs/load.html#cache_get_data)

Notes
: Since 2.1

### integrate_clean_cache

```php
call_integration_hook('integrate_clean_cache')
```


Called from
: [`clean_cache()` in `./Sources/Load.php`](../docs/load.html#clean_cache)

Notes
: Since 2.1

### integrate_set_avatar_data

```php
call_integration_hook('integrate_set_avatar_data', array(&$image, &$data))
```

Type|Parameter|Description
---|---|---
`array`|`&$image`|desc
`array`|`&$data`|desc

Called from
: [`set_avatar_data()` in `./Sources/Load.php`](../docs/load.html#set_avatar_data)

Notes
: Since 2.1

