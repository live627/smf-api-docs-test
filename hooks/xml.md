---
layout: default
group: hooks
title: XML / AJAX
---
* auto-gen TOC:
{:toc}

### integrate_XMLhttpMain_subActions

```php
call_integration_hook('integrate_XMLhttpMain_subActions', array(&$subActions)
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|Hashmap of subactions (`$_GET['sa']`)

Called from
: `XMLhttpMain()` in `./Sources/Xml.php`

Notes
: This is a regular PHP [`callable`](https://www.php.net/manual/en/language.types.callable.php), called with [`call_user_func()`](https://www.php.net/manual/en/function.call-user-func.php) As such, static methods are allowed(`MyClass::myMethod`).
: The result is that, when you navigate to `./index.php?action=xmlhttp;sa=mysubaction`, the function `myFunction()` is called.

*Example usage*

```php
function my_xml_subactions(&$subActions)
{
	$subActions['mysubaction'] = 'myFunction';
}
```
