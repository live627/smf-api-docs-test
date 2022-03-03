---
layout: default
group: hooks
title: XML / AJAX
count: 4
---
* auto-gen TOC:
{:toc}
## News.php
### integrate_xmlfeeds

```php
call_integration_hook('integrate_xmlfeeds', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ShowXmlFeed()` in `./Sources/News.php`](../docs/news.html#showxmlfeed)

Notes
: Since 2.1

### integrate_xml_data

```php
call_integration_hook('integrate_xml_data', array(&$xml_data, &$feed_meta, &$namespaces, &$extraFeedTags, &$forceCdataKeys, &$nsKeys, $xml_format, $subaction, &$doctype))
```

Type|Parameter|Description
---|---|---
`array`|`&$xml_data`|desc
`array`|`&$feed_meta`|desc
`array`|`&$namespaces`|desc
`array`|`&$extraFeedTags`|desc
`array`|`&$forceCdataKeys`|desc
`array`|`&$nsKeys`|desc
`array`|`$xml_format`|desc
`array`|`$subaction`|desc
`array`|`&$doctype`|desc

Called from
: [`buildXmlFeed()` in `./Sources/News.php`](../docs/news.html#buildxmlfeed)

Notes
: Since 2.1

### integrate_fix_url

```php
call_integration_hook('integrate_fix_url', array(&$val))
```

Type|Parameter|Description
---|---|---
`string`|`&$val`|A string containing a possible URL

Called from
: [`fix_possible_url()` in `./Sources/News.php`](../docs/news.html#fix_possible_url)

Notes
: Since 1.1

## Xml.php
### integrate_XMLhttpMain_subActions

```php
call_integration_hook('integrate_XMLhttpMain_subActions', array(&$subActions)
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|Hashmap of subactions (`$_GET['sa']`)

Called from
: [`XMLhttpMain()` in `./Sources/Xml.php`](../docs/xml.html#xmlhttpmain)

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
