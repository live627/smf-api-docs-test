---
layout: default
group: hooks
title: index.template.php
count: 1
---
* auto-gen TOC:
{:toc}
### integrate_' . $list_class . '_quickbuttons

```php
call_integration_hook('integrate_' . $list_class . '_quickbuttons', array(&$list_items))
```

Type|Parameter|Description
---|---|---
`array`|`&$list_items`|desc

Called from
: [`template_quickbuttons()` in `./Themes/default/index.template.php`](../docs/index-template.html#template_quickbuttons)

Notes
: Since 2.1

