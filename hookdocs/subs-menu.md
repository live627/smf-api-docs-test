---
layout: default
group: hooks
title: Subs-Menu.php
count: 1
---
* auto-gen TOC:
{:toc}
### integrate_' . $menu_context['current_action'] . '_areas

```php
call_integration_hook('integrate_' . $menu_context['current_action'] . '_areas', array(&$menuData))
```

Type|Parameter|Description
---|---|---
`array`|`&$menuData`|desc

Called from
: [`createMenu()` in `./Sources/Subs-Menu.php`](../docs/subs-menu.html#createmenu)

Notes
: Since 2.1

