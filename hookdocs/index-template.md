---
layout: default
group: hooks
title: index.template.php
count: 0
---
* auto-gen TOC:
{:toc}
### 

```php
call_integration_hook('integrate_' . $list_class . '_quickbuttons', array(&$list_items))
```

Type|Parameter|Description
---|---|---
`array`|`$&list_items`|desc

Called from
: [`template_quickbuttons()` in `./Themes/default/index.template.php`](../docs/index-template.html#template_quickbuttons)

Notes
: Since 2.1

