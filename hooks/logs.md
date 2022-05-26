---
layout: default
group: hooks
title: Logs
count: 3
---
* auto-gen TOC:
{:toc}

## Errors.php
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


## Logging.php
### integrate_log_types

```php
call_integration_hook('integrate_log_types', array(&$log_types, &$always_log))
```

Type|Parameter|Description
---|---|---
`array`|`&$log_types`|desc
`array`|`&$always_log`|desc

Called from
: [`logActions()` in `./Sources/Logging.php`](../docs/logging.html#logactions)

Notes
: Since 2.1

