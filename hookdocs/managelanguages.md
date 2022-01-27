---
layout: default
group: hooks
title: ManageLanguages.php
count: 5
---
* auto-gen TOC:
{:toc}
### integrate_manage_languages

```php
call_integration_hook('integrate_manage_languages', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageLanguages()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#managelanguages)

Notes
: Since 2.1

### integrate_language_settings

```php
call_integration_hook('integrate_language_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyLanguageSettings()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguagesettings)

Notes
: Since 2.1

### integrate_save_language_settings

```php
call_integration_hook('integrate_save_language_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyLanguageSettings()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguagesettings)

Notes
: Since 2.1

### integrate_modifylanguages

```php
call_integration_hook('integrate_modifylanguages', array(&$themes, &$lang_dirs, &$allows_add_remove, &$additional_string_types))
```

Type|Parameter|Description
---|---|---
`array`|`$&themes`|desc
`array`|`$&lang_dirs`|desc
`array`|`$&allows_add_remove`|desc
`array`|`$&additional_string_types`|desc

Called from
: [`ModifyLanguage()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguage)

Notes
: Since 2.1

### integrate_language_edit_helptext

```php
call_integration_hook('integrate_language_edit_helptext', array(&$special_groups))
```

Type|Parameter|Description
---|---|---
`array`|`$&special_groups`|desc

Called from
: [`ModifyLanguage()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguage)

Notes
: Since 2.1

