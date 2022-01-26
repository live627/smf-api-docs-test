---
layout: default
group: func
navtitle: Subs-Menu.php
title: ./Sources/Subs-Menu.php
count: 2
---
* auto-gen TOC:
{:toc}
### createMenu

```php
function createMenu(array $menuData, array $menuOptions = array()): bool|array
```
Create a menu.



Type|Parameter|Description
---|---|---
`array`|`$menuData`|An array of menu data
`array`|`$menuOptions`|An array of menu options

### destroyMenu

```php
function destroyMenu(string $menu_id = 'last'): bool|void
```
Delete a menu.



Type|Parameter|Description
---|---|---
`string`|`$menu_id`|The ID of the menu to destroy or 'last' for the most recent one

