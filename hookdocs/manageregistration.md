---
layout: default
group: hooks
title: ManageRegistration.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_registrations

```php
call_integration_hook('integrate_manage_registrations', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`RegCenter()` in `./Sources/ManageRegistration.php`](../docs/manageregistration.html#regcenter)

Notes
: Since 2.1

### integrate_modify_registration_settings

```php
call_integration_hook('integrate_modify_registration_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyRegistrationSettings()` in `./Sources/ManageRegistration.php`](../docs/manageregistration.html#modifyregistrationsettings)

Notes
: Since 2.1

### integrate_save_registration_settings

```php
call_integration_hook('integrate_save_registration_settings')
```


Called from
: [`ModifyRegistrationSettings()` in `./Sources/ManageRegistration.php`](../docs/manageregistration.html#modifyregistrationsettings)

Notes
: Since 2.1

