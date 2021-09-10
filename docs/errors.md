---
layout: default
group: func
navtitle: Errors.php
title: ./Sources/Errors.php
count: 10
---
* auto-gen TOC:
{:toc}
### log_error

```php
function log_error($error_message, $error_type = 'general', $file = null, $line = null)
```
Log an error, if the error logging is enabled.

filename and line should be __FILE__ and __LINE__, respectively.
Example use:
 die(log_error($msg));

Type|Parameter|Description
---|---|---
`string`|`$error_message`|The message to log
`string&#124;bool`|`$error_type`|The type of error
`string`|`$file`|The name of the file where this error occurred
`int`|`$line`|The line where the error occurred

### fatal_error

```php
function fatal_error($error, $log = 'general', $status = 500)
```
An irrecoverable error. This function stops execution and displays an error message.

It logs the error message if $log is specified.

Type|Parameter|Description
---|---|---
`string`|`$error`|The error message
`string&#124;bool`|`$log`|= 'general' What type of error to log this as (false to not log it))
`int`|`$status`|The HTTP status code associated with this error

### fatal_lang_error

```php
function fatal_lang_error($error, $log = 'general', $sprintf = array(), $status = 403)
```
Shows a fatal error with a message stored in the language file.

This function stops execution and displays an error message by key.
- uses the string with the error_message_key key.
- logs the error in the forum's default language while displaying the error
  message in the user's language.
- uses Errors language file and applies the $sprintf information if specified.
- the information is logged if log is specified.

Type|Parameter|Description
---|---|---
`string`|`$error`|The error message
`string&#124;false`|`$log`|The type of error, or false to not log it
`array`|`$sprintf`|An array of data to be sprintf()'d into the specified message
`int`|`$status`|= false The HTTP status code associated with this error

### smf_error_handler

```php
function smf_error_handler($error_level, $error_string, $file, $line)
```
Handler for standard error messages, standard PHP error handler replacement.

It dies with fatal_error() if the error_level matches with error_reporting.

Type|Parameter|Description
---|---|---
`int`|`$error_level`|A pre-defined error-handling constant (see {@link https://php.net/errorfunc.constants})
`string`|`$error_string`|The error message
`string`|`$file`|The file where the error occurred
`int`|`$line`|The line where the error occurred

### setup_fatal_error_context

```php
function setup_fatal_error_context($error_message, $error_code = null)
```
It is called by {@link fatal_error()} and {@link fatal_lang_error()}.



Type|Parameter|Description
---|---|---
`string`|`$error_message`|The error message
`string`|`$error_code`|An error code

### display_maintenance_message

```php
function display_maintenance_message()
```
Show a message for the (full block) maintenance mode.

It shows a complete page independent of language files or themes.
It is used only if $maintenance = 2 in Settings.php.
It stops further execution of the script.

### display_db_error

```php
function display_db_error()
```
Show an error message for the connection problems.

It shows a complete page independent of language files or themes.
It is used only if there's no way to connect to the database.
It stops further execution of the script.

### display_loadavg_error

```php
function display_loadavg_error()
```
Show an error message for load average blocking problems.

It shows a complete page independent of language files or themes.
It is used only if the load averages are too high to continue execution.
It stops further execution of the script.

### set_fatal_error_headers

```php
function set_fatal_error_headers()
```
Small utility function for fatal error pages.

Used by {@link display_db_error()}, {@link display_loadavg_error()},
{@link display_maintenance_message()}

### log_error_online

```php
function log_error_online($error, $sprintf = array())
```
Small utility function for fatal error pages.

Used by fatal_error(), fatal_lang_error()

Type|Parameter|Description
---|---|---
`string`|`$error`|The error
`array`|`$sprintf`|An array of data to be sprintf()'d into the specified message

