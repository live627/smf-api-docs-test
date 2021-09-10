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
function createMenu($menuData, $menuOptions = array())
```
Create a menu.



Type|Parameter|Description
---|---|---
`array`|`$menuData`|An array of menu data
`array`|`$menuOptions`|An array of menu options

### destroyMenu

```php
function destroyMenu($menu_id = 'last')
```
Delete a menu.



Type|Parameter|Description
---|---|---
`string`|`$menu_id`|The ID of the menu to destroy or 'last' for the most recent one

