---
layout: default
group: hooks
title: Subs-Themes.php
count: 4
---
* auto-gen TOC:
{:toc}
### integrate_get_single_theme

```php
call_integration_hook('integrate_get_single_theme', array(&$variables, $id))
```

Type|Parameter|Description
---|---|---
`array`|`&$variables`|desc
`array`|`$id`|desc

Called from
: [`get_single_theme()` in `./Sources/Subs-Themes.php`](../docs/subs-themes.html#get_single_theme)

Notes
: Since 2.1

### integrate_get_all_themes

```php
call_integration_hook('integrate_get_all_themes', array(&$themeValues, $enable_only))
```

Type|Parameter|Description
---|---|---
`array`|`&$themeValues`|desc
`array`|`$enable_only`|desc

Called from
: [`get_all_themes()` in `./Sources/Subs-Themes.php`](../docs/subs-themes.html#get_all_themes)

Notes
: Since 2.1

### integrate_get_installed_themes

```php
call_integration_hook('integrate_get_installed_themes', array(&$themeValues))
```

Type|Parameter|Description
---|---|---
`array`|`&$themeValues`|desc

Called from
: [`get_installed_themes()` in `./Sources/Subs-Themes.php`](../docs/subs-themes.html#get_installed_themes)

Notes
: Since 2.1

### integrate_theme_install

```php
call_integration_hook('integrate_theme_install', array(&$context['to_install'], $id_theme))
```

Type|Parameter|Description
---|---|---
`array`|`&$to_install`|desc
`array`|`$id_theme`|desc

Called from
: [`theme_install()` in `./Sources/Subs-Themes.php`](../docs/subs-themes.html#theme_install)

Notes
: Since 2.1

