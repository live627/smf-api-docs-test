---
layout: default
group: hooks
title: Profile-Export.php
count: 5
---
* auto-gen TOC:
{:toc}
### integrate_export_xslt_variables

```php
call_integration_hook('integrate_export_xslt_variables', array(&$xslt_variables, $format))
```

Type|Parameter|Description
---|---|---
`array`|`$&xslt_variables`|desc
`array`|`$format`|desc

Called from
: [`get_xslt_stylesheet()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#get_xslt_stylesheet)

Notes
: Since 2.1

### integrate_export_xslt_stylesheet

```php
call_integration_hook('integrate_export_xslt_stylesheet', array(&$stylesheet, $format))
```

Type|Parameter|Description
---|---|---
`array`|`$&stylesheet`|desc
`array`|`$format`|desc

Called from
: [`get_xslt_stylesheet()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#get_xslt_stylesheet)

Notes
: Since 2.1

### integrate_pre_css_output

```php
call_integration_hook('integrate_pre_css_output')
```


Called from
: [`export_load_css_js()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#export_load_css_js)

Notes
: Since 2.1

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(false))
```

Type|Parameter|Description
---|---|---
`array`|`$false`|desc

Called from
: [`export_load_css_js()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#export_load_css_js)

Notes
: Since 2.1

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(true))
```

Type|Parameter|Description
---|---|---
`array`|`$true`|desc

Called from
: [`export_load_css_js()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#export_load_css_js)

Notes
: Since 2.1

