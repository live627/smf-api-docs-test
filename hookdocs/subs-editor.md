---
layout: default
group: hooks
title: Subs-Editor.php
count: 8
---
* auto-gen TOC:
{:toc}
### integrate_load_message_icons

```php
call_integration_hook('integrate_load_message_icons', array(&$icons))
```

Type|Parameter|Description
---|---|---
`array`|`&$icons`|desc

Called from
: [`getMessageIcons()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#getmessageicons)

Notes
: Since 2.1

### integrate_bbc_buttons

```php
call_integration_hook('integrate_bbc_buttons', array(&$context['bbc_tags'], &$editor_tag_map))
```

Type|Parameter|Description
---|---|---
`array`|`&$bbc_tags`|desc
`array`|`&$editor_tag_map`|desc

Called from
: [`create_control_richedit()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#create_control_richedit)

Notes
: Since 2.1

### integrate_sceditor_options

```php
call_integration_hook('integrate_sceditor_options', array(&$sce_options))
```

Type|Parameter|Description
---|---|---
`array`|`&$sce_options`|desc

Called from
: [`create_control_richedit()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#create_control_richedit)

Notes
: Since 2.1

### integrate_create_control_verification_pre

```php
call_integration_hook('integrate_create_control_verification_pre', array(&$verificationOptions, $do_test))
```

Type|Parameter|Description
---|---|---
`array`|`&$verificationOptions`|desc
`array`|`$do_test`|desc

Called from
: [`create_control_verification()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#create_control_verification)

Notes
: Since 2.1

### integrate_create_control_verification_test

```php
call_integration_hook('integrate_create_control_verification_test', array($thisVerification, &$verification_errors))
```

Type|Parameter|Description
---|---|---
`array`|`$thisVerification`|desc
`array`|`&$verification_errors`|desc

Called from
: [`create_control_verification()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#create_control_verification)

Notes
: Since 2.1

### integrate_create_control_verification_refresh

```php
call_integration_hook('integrate_create_control_verification_refresh', array($thisVerification))
```

Type|Parameter|Description
---|---|---
`array`|`$thisVerification`|desc

Called from
: [`create_control_verification()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#create_control_verification)

Notes
: Since 2.1

### integrate_create_control_verification_post

```php
call_integration_hook('integrate_create_control_verification_post', array(&$verification_errors, $do_test))
```

Type|Parameter|Description
---|---|---
`array`|`&$verification_errors`|desc
`array`|`$do_test`|desc

Called from
: [`create_control_verification()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#create_control_verification)

Notes
: Since 2.1

### integrate_autosuggest

```php
call_integration_hook('integrate_autosuggest', array(&$searchTypes))
```

Type|Parameter|Description
---|---|---
`array`|`&$searchTypes`|desc

Called from
: [`AutoSuggestHandler()` in `./Sources/Subs-Editor.php`](../docs/subs-editor.html#autosuggesthandler)

Notes
: Since 2.1

