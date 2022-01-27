---
layout: default
group: hooks
title: Administrative
---
* auto-gen TOC:
{:toc}

### integrate_admin_search

```php
call_integration_hook('integrate_admin_search', array(&$language_files, &$include_files, &$settings_search)
```

Type|Parameter|Description
---|---|---
`string[]`|`&$language_files`|List of language files that contain the `$txt` keys for the settings
`string[]`|`&$include_files`|List of source files to load
`array`|`&$settings_search`|List of query strings to asssocate with functions

Called from
: [`AdminSearch()` in `./Sources/Admin.php`](../docs/admin.html#adminsearch)

Notes
: Since 2.1
: Each element of `&$urls` has the following definition:

    Type|Key|Description
    ---|---|---
    `string`|`0`|Name of a function to search
    `string`|`1`|Partial querystring to assemble result links

: Will not search the followwing typeds:
    - permissions
    - desc

*Example usage*

```php
function my_admin_search(array &$language_files, array &$include_files, array &$settings_search)
{
	// We have our search language strings in MyLang language file
	$language_files[] = 'MyLang';

	// Include the file that contains the search settings info for our section.
	$include_files[] = 'MySourceFile';

	// Add our search from the following function
	$settings_search[] = array('MyModSettings', 'area=modifications;sa=mymod');
}
```
And in MySourceFile.php, return `$config_vars` when `$return_config` is `true`.
function MyModSettings(bool $return_config = false)
{
	$config_vars = // array...

	if ($return_config)
		return $config_vars;
}
```

```php
call_integration_hook('integrate_modify_modifications', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|

Called from
: [`ModifyModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymodsettings)

Notes
: Since 2.0

### integrate_general_mod_settings

```php
call_integration_hook('integrate_general_mod_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|

Called from
: [`ModifyGeneralModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifygeneralmodsettings)

Notes
: Since 2.0

### integrate_save_general_mod_settings

```php
call_integration_hook('integrate_save_general_mod_settings', array(&$save_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$save_vars`|

Called from
: [`ModifyGeneralModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifygeneralmodsettings)

Notes
: Since 2.1

	// Add our search from the following function
	$settings_search[] = array('MyModSettings', 'area=modifications;sa=mymod');
}
```
And in MySourceFile.php, return `$config_vars` when `$return_config` is `true`.
function MyModSettings(bool $return_config = false)
{
	$config_vars = // array...

	if ($return_config)
		return $config_vars;
}
```
