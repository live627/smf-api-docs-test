---
layout: default
group: hooks
title: Extending the application
---
* auto-gen TOC:
{:toc}
### integrate_actions

```php
call_integration_hook('integrate_actions', array(&$actionArray)
```

Type|Parameter|Description
---|---|---
`array`|`&$actionArray`|Array containing all the actions provided by SMF.

Called from
: `smf_main()` in `./index.php`

Notes
: This is a regular PHP [`callable`](https://www.php.net/manual/en/language.types.callable.php), called with [`call_user_func()`](https://www.php.net/manual/en/function.call-user-func.php) As such, static methods are allowed(`MyClass::myMethod`).
: The result is that, when you navigate to `./index.php?action=myNewAction`, the file `myFile.php` in the Sources directory is loaded and the function `myFunction()` is called.

*Example usage*

```php
function my_actions(&$actionArray)
{
	$actionArray['myNewAction'] = array('myFile.php', 'myFunction');
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
: `loadTheme()` in `./Sources/Load.php`

Notes
: XML mode loads the XML template file, removes any template layers, and pumps out the correct `Content-Type` header.
: Currently ?area=popup and any other simple actions that don't actually exist (e.g. you intended to use ?action=myAction;area=simpleArea but call just ?area=simpleArea) then the board index loads without full templates) If any of the URL schemes above apply then the index template will not be loaded.
: You should avoid generic areas and subactions for this purpose as they may break other mods using similar names (they will no longer load templates as expected).

*Example usage*

```php
function my_simple_actions(&$simpleActions, &$simpleAreas, $simpleSubActions, &$extraParams, &$xmlActions)
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
``

### integrate_autoload

```php
call_integration_hook('integrate_autoload', array(&$classMap)
```

Type|Parameter|Description
---|---|---
`array`|`&$classMap`|Hashmap of [PSR-4](https://www.php-fig.org/psr/psr-4/) namespaces

Notes
: The namespaced files are assumed to be in `$sourcedir` (`./Sources`).

*Example usage*
```php
function my_autoload(&$classMap)
{
	$classMap['My\\Namespace\\'] = 'path/to/files/';
}
```
