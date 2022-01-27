---
layout: default
group: hooks
title: ManageMail.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_mail

```php
call_integration_hook('integrate_manage_mail', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageMail()` in `./Sources/ManageMail.php`](../docs/managemail.html#managemail)

Notes
: Since 2.1

### integrate_modify_mail_settings

```php
call_integration_hook('integrate_modify_mail_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyMailSettings()` in `./Sources/ManageMail.php`](../docs/managemail.html#modifymailsettings)

Notes
: Since 2.1

### integrate_save_mail_settings

```php
call_integration_hook('integrate_save_mail_settings')
```


Called from
: [`ModifyMailSettings()` in `./Sources/ManageMail.php`](../docs/managemail.html#modifymailsettings)

Notes
: Since 2.1

