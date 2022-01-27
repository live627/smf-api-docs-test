---
layout: default
group: hooks
title: ManagePermissions.php
count: 8
---
* auto-gen TOC:
{:toc}
### integrate_manage_permissions

```php
call_integration_hook('integrate_manage_permissions', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ModifyPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#modifypermissions)

Notes
: Since 2.1

### integrate_modify_permission_settings

```php
call_integration_hook('integrate_modify_permission_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`GeneralPermissionSettings()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#generalpermissionsettings)

Notes
: Since 2.1

### integrate_save_permission_settings

```php
call_integration_hook('integrate_save_permission_settings')
```


Called from
: [`GeneralPermissionSettings()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#generalpermissionsettings)

Notes
: Since 2.1

### integrate_load_permission_levels

```php
call_integration_hook('integrate_load_permission_levels', array(&$groupLevels, &$boardLevels))
```

Type|Parameter|Description
---|---|---
`array`|`$&groupLevels`|desc
`array`|`$&boardLevels`|desc

Called from
: [`setPermissionLevel()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#setpermissionlevel)

Notes
: Since 2.1

### integrate_load_permissions

```php
call_integration_hook('integrate_load_permissions', array(&$permissionGroups, &$permissionList, &$leftPermissionGroups, &$hiddenPermissions, &$relabelPermissions))
```

Type|Parameter|Description
---|---|---
`array`|`$&permissionGroups`|desc
`array`|`$&permissionList`|desc
`array`|`$&leftPermissionGroups`|desc
`array`|`$&hiddenPermissions`|desc
`array`|`$&relabelPermissions`|desc

Called from
: [`loadAllPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#loadallpermissions)

Notes
: Since 2.1

### integrate_load_illegal_permissions

```php
call_integration_hook('integrate_load_illegal_permissions')
```


Called from
: [`loadIllegalPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#loadillegalpermissions)

Notes
: Since 2.1

### integrate_load_illegal_guest_permissions

```php
call_integration_hook('integrate_load_illegal_guest_permissions')
```


Called from
: [`loadIllegalGuestPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#loadillegalguestpermissions)

Notes
: Since 2.1

### integrate_post_moderation_mapping

```php
call_integration_hook('integrate_post_moderation_mapping', array(&$mappings))
```

Type|Parameter|Description
---|---|---
`array`|`$&mappings`|desc

Called from
: [`ModifyPostModeration()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#modifypostmoderation)

Notes
: Since 2.1

