---
layout: default
group: hooks
title: Subs-Menu.php
count: 0
---
* auto-gen TOC:
{:toc}
### 

```php
call_integration_hook('integrate_' . $menu_context['current_action'] . '_areas', array(&$menuData))
```

Type|Parameter|Description
---|---|---
`array`|`$&menuData`|desc

Called from
: [`createMenu()` in `./Sources/Subs-Menu.php`](../docs/subs-menu.html#createmenu)

Notes
: Since 2.1

