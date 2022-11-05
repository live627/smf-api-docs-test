---
layout: default
group: hooks
title: Extending the application
count: 5
---
{:toc}
## Help.php
### integrate_manage_help

```php
call_integration_hook('integrate_manage_help', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|Array of subacctions
 | | - Keys correlate to `$_GET['sa']`
 | | - Values are  regular PHP [`callable`](https://www.php.net/manual/en/language.types.callable.php)s, called with [`call_user_func()`](https://www.php.net/manual/en/function.call-user-func.php) As such, static methods are allowed(`MyClass::myMethod`)

Called from
: [`ShowHelp()` in `./Sources/Help.php`](../docs/help.html#showhelp)

Notes
: Since 2.1

*Example usage*

```php
function manage_help(array &$subActions)
{
	$subActions['subaction'] = 'MyFunction';
}
```

### integrate_helpadmin

```php
call_integration_hook('integrate_helpadmin')
```

Called from
: [`ShowAdminHelp()` in `./Sources/Help.php`](../docs/help.html#showadminhelp)

Notes
: Since 2.1
: Allows mods to load their own language files

*Example usage*

```php
function my_helpadmin()
{
	loadLanguage('MyLanguageFile');
}
```

## index.php
### integrate_autoload

```php
call_integration_hook('integrate_autoload', array(&$classMap)
```

Type|Parameter|Description
---|---|---
`array`|`&$classMap`|Hashmap of [PSR-4](https://www.php-fig.org/psr/psr-4/) namespaces

Called from
: `./index.php`

Notes
: Since 2.1
: The namespaced files are assumed to be in `$sourcedir` (`./Sources`).

*Example usage*
```php
function my_autoload(array &$classMap)
{
	$classMap['My\\Namespace\\'] = 'path/to/files/';
}
```

### integrate_actions

```php
call_integration_hook('integrate_actions', array(&$actionArray)
```

Type|Parameter|Description
---|---|---
`array`|`&$actionArray`|Array containing all the actions provided by SMF.

Called from
: [`smf_main()` in `./index.php`](../docs/#smf_main)

Notes
: Since 2.0
: This is a regular PHP [`callable`](https://www.php.net/manual/en/language.types.callable.php), called with [`call_user_func()`](https://www.php.net/manual/en/function.call-user-func.php) As such, static methods are allowed(`MyClass::myMethod`).
: The files are assumed to be in `$sourcedir` (`./Sources`).
: The result is that, when you navigate to `./index.php?action=mynewaction`, the file `MyFile.php` in the Sources directory is loaded and the function `MyFunction()` is called.
: If a mod is using `integrate_autoload`, it should set the first param in each `$actionArray` entry to the boolean value `false` to avoid redundant calls to `require_once`.

*Example usage*

```php
function my_actions(array &$actionArray)
{
	$actionArray['mynewaction'] = array('MyFile.php', 'MyFunction');
}
```

### integrate_simple_actions

```php
call_integration_hook('integrate_simple_actions', array(&$simpleActions, &$simpleAreas, &$simpleSubActions, &$extraParams, &$xmlActions)
```

Type|Parameter|Description
---|---|---
`array`|`&$simpleActions`|List of actions (`$_GET['action']`)
`array`|`&$simpleSubActions`|Parent action => array of areas (`$_GET['area']`)
`array`|`&$simpleSubActions`|Parent action => array of subactions (`$_GET['sa']`)
`array`|`&$extraParams`|List of request params that trigger XML output regardless of the presence of other params
`array`|`&$xmlActions`|List of actions that specifically use XML output (but still require `?xml`)

Called from
: [`loadTheme()` in `./Sources/Load.php`](../docs/load.html#loadtheme)

Notes
: Since 2.1
: XML mode loads the XML template file, removes any template layers, and pumps out the correct `Content-Type` header.
: Currently ?area=popup and any other simple actions that don't actually exist (e.g. you intended to use ?action=myAction;area=simpleArea but call just ?area=simpleArea) then the board index loads without full templates) If any of the URL schemes above apply then the index template will not be loaded.
: You should avoid generic areas and subactions for this purpose as they may break other mods using similar names (they will no longer load templates as expected).

*Example usage*

```php
function my_simple_actions(array &$simpleActions, array &$simpleAreas, array $simpleSubActions, array &$extraParams, array &$xmlActions)
{
	// Applies to /index.php?action=mysimpleaction
	$simpleActions[] = 'mysimpleaction';

	// Applies to /index.php?area=mysimplearea
	$simpleAreas['mysimpleaction'] = ['mysimplearea'];

	// Applies to /index.php?sa=mysimplesubaction
	$simpleSubActions['mysimpleaction'] = ['mysimplesubaction'];

	// Applies to /index.php?myextraparamforxml
	$extraParams[] = 'myextraparamforxml';

	// Applies to /index.php?action=myxmlaction
	$xmlActions[] = 'myxmlaction';
}
```
