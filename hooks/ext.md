---
layout: default
group: hooks
title: Extedding the application
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

Example usage
: ```php
function my_actions(&$actionArray)
{
	$actionArray['myNewAction'] = array('myFile.php', 'myFunction');
}```
: The result is that, when you navigate to `./index.php?action=myNewAction`, the file `myFile.php` in the Sources directory is loaded and the function `myFunction()` is called.
