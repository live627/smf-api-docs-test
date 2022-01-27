---
layout: default
group: hooks
title: ManageSmileys.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_smileys

```php
call_integration_hook('integrate_manage_smileys', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageSmileys()` in `./Sources/ManageSmileys.php`](../docs/managesmileys.html#managesmileys)

Notes
: Since 2.1

### integrate_modify_smiley_settings

```php
call_integration_hook('integrate_modify_smiley_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`EditSmileySettings()` in `./Sources/ManageSmileys.php`](../docs/managesmileys.html#editsmileysettings)

Notes
: Since 2.1

### integrate_save_smiley_settings

```php
call_integration_hook('integrate_save_smiley_settings')
```


Called from
: [`EditSmileySettings()` in `./Sources/ManageSmileys.php`](../docs/managesmileys.html#editsmileysettings)

Notes
: Since 2.1

