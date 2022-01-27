---
layout: default
group: hooks
title: News.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_xmlfeeds

```php
call_integration_hook('integrate_xmlfeeds', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

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
`array`|`$&xml_data`|desc
`array`|`$&feed_meta`|desc
`array`|`$&namespaces`|desc
`array`|`$&extraFeedTags`|desc
`array`|`$&forceCdataKeys`|desc
`array`|`$&nsKeys`|desc
`array`|`$xml_format`|desc
`array`|`$subaction`|desc
`array`|`$&doctype`|desc

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
`array`|`$&val`|desc

Called from
: [`fix_possible_url()` in `./Sources/News.php`](../docs/news.html#fix_possible_url)

Notes
: Since 2.1

