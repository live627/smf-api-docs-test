---
layout: default
group: func
navtitle: GenericMenu.template.php
title: ./Themes/default/GenericMenu.template.php
count: 4
---
* auto-gen TOC:
{:toc}
### template_generic_menu_dropdown_above

```php
function template_generic_menu_dropdown_above(): void
```
This contains the HTML for the menu bar at the top of the admin center.



### template_generic_menu_dropdown_below

```php
function template_generic_menu_dropdown_below(): void
```
Part of the admin layer - used with generic_menu_dropdown_above to close the admin content div.



### template_generic_menu

```php
function template_generic_menu(array &$menu_context): void
```
The template for displaying a menu



Type|Parameter|Description
---|---|---
`array`|`$menu_context`|An array of menu information

### template_generic_menu_tabs

```php
function template_generic_menu_tabs(array &$menu_context): void
```
The code for displaying the menu



Type|Parameter|Description
---|---|---
`array`|`$menu_context`|An array of menu context data

