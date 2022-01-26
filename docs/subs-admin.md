---
layout: default
group: func
navtitle: Subs-Admin.php
title: ./Sources/Subs-Admin.php
count: 11
---
* auto-gen TOC:
{:toc}
### getServerVersions

```php
function getServerVersions(array $checkFor): array
```
Get a list of versions that are currently installed on the server.



Type|Parameter|Description
---|---|---
`array`|`$checkFor`|An array of what to check versions for - can contain one or more of 'gd', 'imagemagick', 'db_server', 'phpa', 'memcache', 'php' or 'server'

### getFileVersions

```php
function getFileVersions(array &$versionOptions): array
```
Search through source, theme and language files to determine their version.

Get detailed version information about the physical SMF files on the server.

- the input parameter allows to set whether to include SSI.php and whether
  the results should be sorted.
- returns an array containing information on source files, templates and
  language files found in the default theme directory (grouped by language).

Type|Parameter|Description
---|---|---
`array`|` &$versionOptions`|An array of options. Can contain one or more of 'include_ssi', 'include_subscriptions', 'include_tasks' and 'sort_results'

### updateSettingsFile

```php
function updateSettingsFile(array $config_vars, ?bool $keep_quotes = null, bool $rebuild = false): bool
```
Update the Settings.php file.

The most important function in this file for mod makers happens to be the
updateSettingsFile() function, but it shouldn't be used often anyway.

- Updates the Settings.php file with the changes supplied in config_vars.

- Expects config_vars to be an associative array, with the keys as the
  variable names in Settings.php, and the values the variable values.

- Correctly formats the values using smf_var_export().

- Restores standard formatting of the file, if $rebuild is true.

- Checks for changes to db_last_error and passes those off to a separate
  handler.

- Creates a backup file and will use it should the writing of the
  new settings file fail.

- Tries to intelligently trim quotes and remove slashes from string values.
  This is done for backwards compatibility purposes (old versions of this
  function expected strings to have been manually escaped and quoted). This
  behaviour can be controlled by the $keep_quotes parameter.

Type|Parameter|Description
---|---|---
`array`|`$config_vars`|An array of one or more variables to update.
`bool&#124;null`|`$keep_quotes`|Whether to strip slashes & trim quotes from string values. Defaults to auto-detection.
`bool`|`$rebuild`|If true, attempts to rebuild with standard format. Default false.

### get_current_settings

```php
function get_current_settings(int $mtime = null, string $settingsFile = null): array
```
Retrieves a copy of the current values of all settings defined in Settings.php.

Importantly, it does this without affecting our actual global variables at all,
and it performs safety checks before acting. The result is an array of the
values as recorded in the settings file.

Type|Parameter|Description
---|---|---
`int`|`$mtime`|Timestamp of last known good configuration. Defaults to time SMF started.
`string`|`$settingsFile`|The settings file. Defaults to SMF's standard Settings.php.

### safe_file_write

```php
function safe_file_write(string $file, string $data, string $backup_file = null, int $mtime = null, bool $append = false): bool
```
Writes data to a file, optionally making a backup, while avoiding race conditions.



Type|Parameter|Description
---|---|---
`string`|`$file`|The filepath of the file where the data should be written.
`string`|`$data`|The data to be written to $file.
`string`|`$backup_file`|The filepath where the backup should be saved. Default null.
`int`|`$mtime`|If modification time of $file is more recent than this Unix timestamp, the write operation will abort. Defaults to time that the script started execution.
`bool`|`$append`|If true, the data will be appended instead of overwriting the existing content of the file. Default false.

### smf_var_export

```php
function smf_var_export(mixed $var): mixed
```
A wrapper around var_export whose output matches SMF coding conventions.



Type|Parameter|Description
---|---|---
`mixed`|`$var`|The variable to export

### strip_php_comments

```php
function strip_php_comments(string $code_str): string
```
Deletes all PHP comments from a string.



Type|Parameter|Description
---|---|---
`string`|`$code_str`|A string containing PHP code.

### updateDbLastError

```php
function updateDbLastError(int $time, bool $update = true): bool
```
Saves the time of the last db error for the error log
- Done separately from updateSettingsFile to avoid race conditions
  which can occur during a db error
- If it fails Settings.php will assume 0



Type|Parameter|Description
---|---|---
`int`|`$time`|The timestamp of the last DB error
`bool`|``|True If we should update the current db_last_error context as well.  This may be useful in cases where the current context needs to know a error was logged since the last check.

### updateAdminPreferences

```php
function updateAdminPreferences(): void
```
Saves the admin's current preferences to the database.



### emailAdmins

```php
function emailAdmins(string $template, array $replacements = array(), array $additional_recipients = array()): void
```
Send all the administrators a lovely email.

- loads all users who are admins or have the admin forum permission.
- uses the email template and replacements passed in the parameters.
- sends them an email.

Type|Parameter|Description
---|---|---
`string`|`$template`|Which email template to use
`array`|`$replacements`|An array of items to replace the variables in the template
`array`|`$additional_recipients`|An array of arrays of info for additional recipients. Should have 'id', 'email' and 'name' for each.

### sm_temp_dir

```php
function sm_temp_dir(): string
```
Locates the most appropriate temp directory.

Systems using `open_basedir` restrictions may receive errors with
`sys_get_temp_dir()` due to misconfigurations on servers. Other
cases sys_temp_dir may not be set to a safe value. Additionally
`sys_get_temp_dir` may use a readonly directory. This attempts to
find a working temp directory that is accessible under the
restrictions and is writable to the web service account.

Directories checked against `open_basedir`:

- `sys_get_temp_dir()`
- `upload_tmp_dir`
- `session.save_path`
- `cachedir`

