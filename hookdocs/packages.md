---
layout: default
group: hooks
title: Packages
count: 3
---
{:toc}
## Packages.php
### integrate_manage_packages

```php
call_integration_hook('integrate_manage_packages', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`Packages()` in `./Sources/Packages.php`](../docs/packages.html#packages)

Notes
: Since 2.1

### integrate_modification_types

```php
call_integration_hook('integrate_modification_types')
```


Called from
: [`PackageBrowse()` in `./Sources/Packages.php`](../docs/packages.html#packagebrowse)

Notes
: Since 2.1

### integrate_packages_sort_id

```php
call_integration_hook('integrate_packages_sort_id', array(&$sort_id, &$packages))
```

Type|Parameter|Description
---|---|---
`array`|`&$sort_id`|desc
`array`|`&$packages`|desc

Called from
: [`list_getPackages()` in `./Sources/Packages.php`](../docs/packages.html#list_getpackages)

Notes
: Since 2.1

