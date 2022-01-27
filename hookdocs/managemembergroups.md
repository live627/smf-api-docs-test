---
layout: default
group: hooks
title: ManageMembergroups.php
count: 7
---
* auto-gen TOC:
{:toc}
### integrate_manage_membergroups

```php
call_integration_hook('integrate_manage_membergroups', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ModifyMembergroups()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#modifymembergroups)

Notes
: Since 2.1

### integrate_pre_add_membergroup

```php
call_integration_hook('integrate_pre_add_membergroup', array())
```

Type|Parameter|Description
---|---|---

Called from
: [`AddMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#addmembergroup)

Notes
: Since 2.1

### integrate_add_membergroup

```php
call_integration_hook('integrate_add_membergroup', array($id_group, $postCountBasedGroup))
```

Type|Parameter|Description
---|---|---
`array`|`$id_group`|desc
`array`|`$postCountBasedGroup`|desc

Called from
: [`AddMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#addmembergroup)

Notes
: Since 2.1

### integrate_save_membergroup

```php
call_integration_hook('integrate_save_membergroup', array((int) $_REQUEST['group']))
```

Type|Parameter|Description
---|---|---
`array`|`???`|desc

Called from
: [`EditMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#editmembergroup)

Notes
: Since 2.1

### integrate_view_membergroup

```php
call_integration_hook('integrate_view_membergroup')
```


Called from
: [`EditMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#editmembergroup)

Notes
: Since 2.1

### integrate_modify_membergroup_settings

```php
call_integration_hook('integrate_modify_membergroup_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyMembergroupsettings()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#modifymembergroupsettings)

Notes
: Since 2.1

### integrate_save_membergroup_settings

```php
call_integration_hook('integrate_save_membergroup_settings')
```


Called from
: [`ModifyMembergroupsettings()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#modifymembergroupsettings)

Notes
: Since 2.1

