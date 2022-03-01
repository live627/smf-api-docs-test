---
layout: default
group: hooks
title: Subs.php
count: 17
---
* auto-gen TOC:
{:toc}

## Subs.php
### integrate_change_member_data

```php
call_integration_hook('integrate_change_member_data', array($member_names, $var, &$data[$var], &$knownInts, &$knownFloats))
```

Type|Parameter|Description
---|---|---
`array`|`$member_names`|desc
`array`|`$var`|desc
`array`|`&$var`|desc
`array`|`&$knownInts`|desc
`array`|`&$knownFloats`|desc

Called from
: [`updateMemberData()` in `./Sources/Subs.php`](../docs/subs.html#updatememberdata)

Notes
: Since 2.1

### integrate_pre_parsebbc

```php
call_integration_hook('integrate_pre_parsebbc', array(&$message, &$smileys, &$cache_id, &$parse_tags))
```

Type|Parameter|Description
---|---|---
`array`|`&$message`|desc
`array`|`&$smileys`|desc
`array`|`&$cache_id`|desc
`array`|`&$parse_tags`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_attach_bbc_validate

```php
call_integration_hook('integrate_attach_bbc_validate', array(&$returnContext, $currentAttachment, $tag, $data, $disabled, $params))
```

Type|Parameter|Description
---|---|---
`array`|`&$returnContext`|desc
`array`|`$currentAttachment`|desc
`array`|`$tag`|desc
`array`|`$data`|desc
`array`|`$disabled`|desc
`array`|`$params`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_bbc_codes

```php
call_integration_hook('integrate_bbc_codes', array(&$codes, &$no_autolink_tags))
```

Type|Parameter|Description
---|---|---
`array`|`&$codes`|desc
`array`|`&$no_autolink_tags`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_bbc_print

```php
call_integration_hook('integrate_bbc_print', array(&$disabled))
```

Type|Parameter|Description
---|---|---
`array`|`&$disabled`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_autolinker_schemes

```php
call_integration_hook('integrate_autolinker_schemes', array(&$schemes))
```

Type|Parameter|Description
---|---|---
`array`|`&$schemes`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_post_parsebbc

```php
call_integration_hook('integrate_post_parsebbc', array(&$message, &$smileys, &$cache_id, &$parse_tags))
```

Type|Parameter|Description
---|---|---
`array`|`&$message`|desc
`array`|`&$smileys`|desc
`array`|`&$cache_id`|desc
`array`|`&$parse_tags`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_smileys

```php
call_integration_hook('integrate_smileys', array(&$smileyPregSearch, &$smileyPregReplacements))
```

Type|Parameter|Description
---|---|---
`array`|`&$smileyPregSearch`|desc
`array`|`&$smileyPregReplacements`|desc

Called from
: [`parsesmileys()` in `./Sources/Subs.php`](../docs/subs.html#parsesmileys)

Notes
: Since 2.1

### integrate_proxy

```php
call_integration_hook('integrate_proxy', array($url, &$proxied_url))
```

Type|Parameter|Description
---|---|---
`array`|`$url`|desc
`array`|`&$proxied_url`|desc

Called from
: [`get_proxied_url()` in `./Sources/Subs.php`](../docs/subs.html#get_proxied_url)

Notes
: Since 2.1

### integrate_redirect

```php
call_integration_hook('integrate_redirect', array(&$setLocation, &$refresh, &$permanent))
```

Type|Parameter|Description
---|---|---
`array`|`&$setLocation`|desc
`array`|`&$refresh`|desc
`array`|`&$permanent`|desc

Called from
: [`redirectexit()` in `./Sources/Subs.php`](../docs/subs.html#redirectexit)

Notes
: Since 2.1

### integrate_exit

```php
call_integration_hook('integrate_exit', array($do_footer))
```

Type|Parameter|Description
---|---|---
`array`|`$do_footer`|desc

Called from
: [`obExit()` in `./Sources/Subs.php`](../docs/subs.html#obexit)

Notes
: Since 2.1

### integrate_theme_context

```php
call_integration_hook('integrate_theme_context')
```


Called from
: [`setupThemeContext()` in `./Sources/Subs.php`](../docs/subs.html#setupthemecontext)

Notes
: Since 2.1

### integrate_security_files

```php
call_integration_hook('integrate_security_files', array(&$securityFiles))
```

Type|Parameter|Description
---|---|---
`array`|`&$securityFiles`|desc

Called from
: [`template_header()` in `./Sources/Subs.php`](../docs/subs.html#template_header)

Notes
: Since 2.1

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(&$do_deferred))
```

Type|Parameter|Description
---|---|---
`array`|`&$do_deferred`|desc

Called from
: [`template_javascript()` in `./Sources/Subs.php`](../docs/subs.html#template_javascript)

Notes
: Since 2.1

### integrate_pre_css_output

```php
call_integration_hook('integrate_pre_css_output')
```


Called from
: [`template_css()` in `./Sources/Subs.php`](../docs/subs.html#template_css)

Notes
: Since 2.1

### integrate_menu_buttons

```php
call_integration_hook('integrate_menu_buttons', array(&$buttons))
```

Type|Parameter|Description
---|---|---
`array`|`&$buttons`|desc

Called from
: [`setupMenuContext()` in `./Sources/Subs.php`](../docs/subs.html#setupmenucontext)

Notes
: Since 2.1

### integrate_current_action

```php
call_integration_hook('integrate_current_action', array(&$current_action))
```

Type|Parameter|Description
---|---|---
`array`|`&$current_action`|desc

Called from
: [`setupMenuContext()` in `./Sources/Subs.php`](../docs/subs.html#setupmenucontext)

Notes
: Since 2.1

