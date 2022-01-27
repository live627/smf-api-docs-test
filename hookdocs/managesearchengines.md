---
layout: default
group: hooks
title: ManageSearchEngines.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_search_engines

```php
call_integration_hook('integrate_manage_search_engines', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`SearchEngines()` in `./Sources/ManageSearchEngines.php`](../docs/managesearchengines.html#searchengines)

Notes
: Since 2.1

### integrate_modify_search_engine_settings

```php
call_integration_hook('integrate_modify_search_engine_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ManageSearchEngineSettings()` in `./Sources/ManageSearchEngines.php`](../docs/managesearchengines.html#managesearchenginesettings)

Notes
: Since 2.1

### integrate_save_search_engine_settings

```php
call_integration_hook('integrate_save_search_engine_settings')
```


Called from
: [`ManageSearchEngineSettings()` in `./Sources/ManageSearchEngines.php`](../docs/managesearchengines.html#managesearchenginesettings)

Notes
: Since 2.1

