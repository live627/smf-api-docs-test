---
layout: default
group: hooks
title: ManageSearch.php
count: 5
---
* auto-gen TOC:
{:toc}
### integrate_manage_search

```php
call_integration_hook('integrate_manage_search', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageSearch()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#managesearch)

Notes
: Since 2.1

### integrate_modify_search_settings

```php
call_integration_hook('integrate_modify_search_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`EditSearchSettings()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editsearchsettings)

Notes
: Since 2.1

### integrate_save_search_settings

```php
call_integration_hook('integrate_save_search_settings')
```


Called from
: [`EditSearchSettings()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editsearchsettings)

Notes
: Since 2.1

### integrate_modify_search_weights

```php
call_integration_hook('integrate_modify_search_weights', array(&$factors))
```

Type|Parameter|Description
---|---|---
`array`|`$&factors`|desc

Called from
: [`EditWeights()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editweights)

Notes
: Since 2.1

### integrate_save_search_weights

```php
call_integration_hook('integrate_save_search_weights')
```


Called from
: [`EditWeights()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editweights)

Notes
: Since 2.1

