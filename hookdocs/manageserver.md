---
layout: default
group: hooks
title: ManageServer.php
count: 17
---
* auto-gen TOC:
{:toc}
### integrate_server_settings

```php
call_integration_hook('integrate_server_settings', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ModifySettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifysettings)

Notes
: Since 2.1

### integrate_general_settings

```php
call_integration_hook('integrate_general_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyGeneralSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsettings)

Notes
: Since 2.1

### integrate_save_general_settings

```php
call_integration_hook('integrate_save_general_settings')
```


Called from
: [`ModifyGeneralSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsettings)

Notes
: Since 2.1

### integrate_database_settings

```php
call_integration_hook('integrate_database_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyDatabaseSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifydatabasesettings)

Notes
: Since 2.1

### integrate_save_database_settings

```php
call_integration_hook('integrate_save_database_settings')
```


Called from
: [`ModifyDatabaseSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifydatabasesettings)

Notes
: Since 2.1

### integrate_cookie_settings

```php
call_integration_hook('integrate_cookie_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyCookieSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifycookiesettings)

Notes
: Since 2.1

### integrate_save_cookie_settings

```php
call_integration_hook('integrate_save_cookie_settings')
```


Called from
: [`ModifyCookieSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifycookiesettings)

Notes
: Since 2.1

### integrate_general_security_settings

```php
call_integration_hook('integrate_general_security_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyGeneralSecuritySettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsecuritysettings)

Notes
: Since 2.1

### integrate_save_general_security_settings

```php
call_integration_hook('integrate_save_general_security_settings')
```


Called from
: [`ModifyGeneralSecuritySettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsecuritysettings)

Notes
: Since 2.1

### integrate_modify_cache_settings

```php
call_integration_hook('integrate_modify_cache_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyCacheSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifycachesettings)

Notes
: Since 2.1

### integrate_save_cache_settings

```php
call_integration_hook('integrate_save_cache_settings')
```


Called from
: [`ModifyCacheSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifycachesettings)

Notes
: Since 2.1

### integrate_export_settings

```php
call_integration_hook('integrate_export_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyExportSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyexportsettings)

Notes
: Since 2.1

### integrate_save_export_settings

```php
call_integration_hook('integrate_save_export_settings')
```


Called from
: [`ModifyExportSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyexportsettings)

Notes
: Since 2.1

### integrate_loadavg_settings

```php
call_integration_hook('integrate_loadavg_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyLoadBalancingSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyloadbalancingsettings)

Notes
: Since 2.1

### integrate_save_loadavg_settings

```php
call_integration_hook('integrate_save_loadavg_settings')
```


Called from
: [`ModifyLoadBalancingSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyloadbalancingsettings)

Notes
: Since 2.1

### integrate_prepare_db_settings

```php
call_integration_hook('integrate_prepare_db_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`prepareDBSettingContext()` in `./Sources/ManageServer.php`](../docs/manageserver.html#preparedbsettingcontext)

Notes
: Since 2.1

### integrate_load_cache_apis

```php
call_integration_hook('integrate_load_cache_apis', array(&$loadedApis))
```

Type|Parameter|Description
---|---|---
`array`|`$&loadedApis`|desc

Called from
: [`loadCacheAPIs()` in `./Sources/ManageServer.php`](../docs/manageserver.html#loadcacheapis)

Notes
: Since 2.1

