---
layout: default
group: hooks
title: ManageSettings.php
count: 23
---
* auto-gen TOC:
{:toc}
### integrate_modify_features

```php
call_integration_hook('integrate_modify_features', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ModifyFeatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifyfeaturesettings)

Notes
: Since 2.1

### integrate_modify_modifications

```php
call_integration_hook('integrate_modify_modifications', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ModifyModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymodsettings)

Notes
: Since 2.1

### integrate_modify_basic_settings

```php
call_integration_hook('integrate_modify_basic_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyBasicSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybasicsettings)

Notes
: Since 2.1

### integrate_save_basic_settings

```php
call_integration_hook('integrate_save_basic_settings')
```


Called from
: [`ModifyBasicSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybasicsettings)

Notes
: Since 2.1

### integrate_modify_bbc_settings

```php
call_integration_hook('integrate_modify_bbc_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyBBCSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybbcsettings)

Notes
: Since 2.1

### integrate_save_bbc_settings

```php
call_integration_hook('integrate_save_bbc_settings', array($bbcTags))
```

Type|Parameter|Description
---|---|---
`array`|`$bbcTags`|desc

Called from
: [`ModifyBBCSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybbcsettings)

Notes
: Since 2.1

### integrate_layout_settings

```php
call_integration_hook('integrate_layout_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyLayoutSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylayoutsettings)

Notes
: Since 2.1

### integrate_save_layout_settings

```php
call_integration_hook('integrate_save_layout_settings')
```


Called from
: [`ModifyLayoutSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylayoutsettings)

Notes
: Since 2.1

### integrate_likes_settings

```php
call_integration_hook('integrate_likes_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyLikesSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylikessettings)

Notes
: Since 2.1

### integrate_save_likes_settings

```php
call_integration_hook('integrate_save_likes_settings')
```


Called from
: [`ModifyLikesSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylikessettings)

Notes
: Since 2.1

### integrate_mentions_settings

```php
call_integration_hook('integrate_mentions_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyMentionsSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymentionssettings)

Notes
: Since 2.1

### integrate_save_mentions_settings

```php
call_integration_hook('integrate_save_mentions_settings')
```


Called from
: [`ModifyMentionsSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymentionssettings)

Notes
: Since 2.1

### integrate_warning_settings

```php
call_integration_hook('integrate_warning_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyWarningSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifywarningsettings)

Notes
: Since 2.1

### integrate_save_warning_settings

```php
call_integration_hook('integrate_save_warning_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&save_vars`|desc

Called from
: [`ModifyWarningSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifywarningsettings)

Notes
: Since 2.1

### integrate_spam_settings

```php
call_integration_hook('integrate_spam_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyAntispamSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifyantispamsettings)

Notes
: Since 2.1

### integrate_save_spam_settings

```php
call_integration_hook('integrate_save_spam_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&save_vars`|desc

Called from
: [`ModifyAntispamSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifyantispamsettings)

Notes
: Since 2.1

### integrate_signature_settings

```php
call_integration_hook('integrate_signature_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifySignatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifysignaturesettings)

Notes
: Since 2.1

### integrate_apply_signature_settings

```php
call_integration_hook('integrate_apply_signature_settings', array(&$sig, $sig_limits, $disabledTags))
```

Type|Parameter|Description
---|---|---
`array`|`$&sig`|desc
`array`|`$sig_limits`|desc
`array`|`$disabledTags`|desc

Called from
: [`ModifySignatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifysignaturesettings)

Notes
: Since 2.1

### integrate_save_signature_settings

```php
call_integration_hook('integrate_save_signature_settings', array(&$sig_limits, &$bbcTags))
```

Type|Parameter|Description
---|---|---
`array`|`$&sig_limits`|desc
`array`|`$&bbcTags`|desc

Called from
: [`ModifySignatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifysignaturesettings)

Notes
: Since 2.1

### integrate_prune_settings

```php
call_integration_hook('integrate_prune_settings', array(&$config_vars, &$prune_toggle, false))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc
`array`|`$&prune_toggle`|desc
`array`|`$false`|desc

Called from
: [`ModifyLogSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylogsettings)

Notes
: Since 2.1

### integrate_prune_settings

```php
call_integration_hook('integrate_prune_settings', array(&$savevar, &$prune_toggle, true))
```

Type|Parameter|Description
---|---|---
`array`|`$&savevar`|desc
`array`|`$&prune_toggle`|desc
`array`|`$true`|desc

Called from
: [`ModifyLogSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylogsettings)

Notes
: Since 2.1

### integrate_general_mod_settings

```php
call_integration_hook('integrate_general_mod_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyGeneralModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifygeneralmodsettings)

Notes
: Since 2.1

### integrate_save_general_mod_settings

```php
call_integration_hook('integrate_save_general_mod_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&save_vars`|desc

Called from
: [`ModifyGeneralModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifygeneralmodsettings)

Notes
: Since 2.1

