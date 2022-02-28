---
layout: default
group: hooks
title: Themes.php
count: 4
---
* auto-gen TOC:
{:toc}
### integrate_manage_themes

```php
call_integration_hook('integrate_manage_themes', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ThemesMain()` in `./Sources/Themes.php`](../docs/themes.html#themesmain)

Notes
: Since 2.1

### integrate_theme_options

```php
call_integration_hook('integrate_theme_options')
```


Called from
: [`SetThemeOptions()` in `./Sources/Themes.php`](../docs/themes.html#setthemeoptions)

Notes
: Since 2.1

### integrate_theme_settings

```php
call_integration_hook('integrate_theme_settings')
```


Called from
: [`SetThemeSettings()` in `./Sources/Themes.php`](../docs/themes.html#setthemesettings)

Notes
: Since 2.1

### integrate_wrap_action

```php
call_integration_hook('integrate_wrap_action')
```


Called from
: [`WrapAction()` in `./Sources/Themes.php`](../docs/themes.html#wrapaction)

Notes
: Since 2.1

