---
layout: default
group: hooks
title: Display
count: 7
---
* auto-gen TOC:
{:toc}
## Display.php
### integrate_display_topic

```php
call_integration_hook('integrate_display_topic', array(&$topic_selects, &$topic_tables, &$topic_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$topic_selects`|desc
`array`|`&$topic_tables`|desc
`array`|`&$topic_parameters`|desc

Called from
: [`Display()` in `./Sources/Display.php`](../docs/display.html#display)

Notes
: Since 2.1

### integrate_poll_buttons

```php
call_integration_hook('integrate_poll_buttons')
```


Called from
: [`Display()` in `./Sources/Display.php`](../docs/display.html#display)

Notes
: Since 2.1

### integrate_display_message_list

```php
call_integration_hook('integrate_display_message_list', array(&$messages, &$posters))
```

Type|Parameter|Description
---|---|---
`array`|`&$messages`|desc
`array`|`&$posters`|desc

Called from
: [`Display()` in `./Sources/Display.php`](../docs/display.html#display)

Notes
: Since 2.1

### integrate_query_message

```php
call_integration_hook('integrate_query_message', array(&$msg_selects, &$msg_tables, &$msg_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$msg_selects`|desc
`array`|`&$msg_tables`|desc
`array`|`&$msg_parameters`|desc

Called from
: [`Display()` in `./Sources/Display.php`](../docs/display.html#display)

Notes
: Since 2.1

### integrate_display_buttons

```php
call_integration_hook('integrate_display_buttons', array(&$context['normal_buttons']))
```

Type|Parameter|Description
---|---|---
`array`|`&$normal_buttons`|desc

Called from
: [`Display()` in `./Sources/Display.php`](../docs/display.html#display)

Notes
: Since 2.1

### integrate_mod_buttons

```php
call_integration_hook('integrate_mod_buttons', array(&$context['mod_buttons']))
```

Type|Parameter|Description
---|---|---
`array`|`&$mod_buttons`|desc

Called from
: [`Display()` in `./Sources/Display.php`](../docs/display.html#display)

Notes
: Since 2.1

### integrate_prepare_display_context

```php
call_integration_hook('integrate_prepare_display_context', array(&$output, &$message, $counter))
```

Type|Parameter|Description
---|---|---
`array`|`&$output`|desc
`array`|`&$message`|desc
`array`|`$counter`|desc

Called from
: [`prepareDisplayContext()` in `./Sources/Display.php`](../docs/display.html#preparedisplaycontext)

Notes
: Since 2.1

