---
layout: default
group: hooks
title: Errors.php
count: 2
---
* auto-gen TOC:
{:toc}
### integrate_error_types

```php
call_integration_hook('integrate_error_types', array(&$other_error_types, &$error_type, $error_message, $file, $line))
```

Type|Parameter|Description
---|---|---
`array`|`&$other_error_types`|desc
`array`|`&$error_type`|desc
`array`|`$error_message`|desc
`array`|`$file`|desc
`array`|`$line`|desc

Called from
: [`log_error()` in `./Sources/Errors.php`](../docs/errors.html#log_error)

Notes
: Since 2.1

### integrate_output_error

```php
call_integration_hook('integrate_output_error', array($message, $error_type, $error_level, $file, $line))
```

Type|Parameter|Description
---|---|---
`array`|`$message`|desc
`array`|`$error_type`|desc
`array`|`$error_level`|desc
`array`|`$file`|desc
`array`|`$line`|desc

Called from
: [`smf_error_handler()` in `./Sources/Errors.php`](../docs/errors.html#smf_error_handler)

Notes
: Since 2.1

