---
layout: default
group: func
navtitle: index.template.php
title: ./Themes/default/index.template.php
count: 11
---
* auto-gen TOC:
{:toc}
### template_init

```php
function template_init(): void
```
Initialize the template... mainly little settings.



### template_html_above

```php
function template_html_above(): void
```
The main sub template above the content.



### template_body_above

```php
function template_body_above(): void
```
The upper part of the main template layer. This is the stuff that shows above the main forum content.



### template_body_below

```php
function template_body_below(): void
```
The stuff shown immediately below the main content, including the footer



### template_html_below

```php
function template_html_below(): void
```
This shows any deferred JavaScript and closes out the HTML



### theme_linktree

```php
function theme_linktree(bool $force_show = false): void
```
Show a linktree. This is that thing that shows "My Community | General Category | General Discussion".

.

Type|Parameter|Description
---|---|---
`bool`|`$force_show`|Whether to force showing it even if settings say otherwise

### template_menu

```php
function template_menu(): void
```
Show the menu up top. Something like [home] [help] [profile] [logout].

..

### template_button_strip

```php
function template_button_strip(array $button_strip, string $direction = '', array $strip_options = array()): void
```
Generate a strip of buttons.



Type|Parameter|Description
---|---|---
`array`|`$button_strip`|An array with info for displaying the strip
`string`|`$direction`|The direction
`array`|`$strip_options`|Options for the button strip

### template_quickbuttons

```php
function template_quickbuttons(array $list_items, string $list_class = null, string $output_method = 'echo'): void|string
```
Generate a list of quickbuttons.



Type|Parameter|Description
---|---|---
`array`|`$list_items`|An array with info for displaying the strip
`string`|`$list_class`|Used for integration hooks and as a class name
`string`|`$output_method`|The output method. If 'echo', simply displays the buttons, otherwise returns the HTML for them

### template_maint_warning_above

```php
function template_maint_warning_above(): void
```
The upper part of the maintenance warning box



### template_maint_warning_below

```php
function template_maint_warning_below(): void
```
The lower part of the maintenance warning box.



