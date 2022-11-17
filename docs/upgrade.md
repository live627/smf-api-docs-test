---
layout: default
group: func
navtitle: upgrade.php
title: ./upgrade.php
count: 48
---
* auto-gen TOC:
{:toc}
### upgradeExit

```php
// Exit the upgrade script.
function upgradeExit($fallThrough = false)
```
### load_lang_file

```php
// Load the list of language files, and the current language file.
function load_lang_file()
```
### redirectLocation

```php
// Used to direct the user to another location.
function redirectLocation($location, $addForm = true)
```
### loadEssentialData

```php
// Load all essential data and connect to the DB as this is pre SSI.php
function loadEssentialData()
```
### initialize_inputs

```php
function initialize_inputs()
```
### WelcomeLogin

```php
// Step 0 - Let's welcome them in and ask them to login!
function WelcomeLogin()
```
### checkFolders

```php
// Do a number of attachment & avatar folder checks.
// Display a warning if issues found.  Does not force a hard stop.
function checkFolders()
```
### checkLogin

```php
// Step 0.5: Does the login work?
function checkLogin()
```
### UpgradeOptions

```php
// Step 1: Do the maintenance and backup.
function UpgradeOptions()
```
### BackupDatabase

```php
// Backup the database - why not...
function BackupDatabase()
```
### backupTable

```php
// Backup one table...
function backupTable($table)
```
### DatabaseChanges

```php
// Step 2: Everything.
function DatabaseChanges()
```
### setSqlMode

```php
// Different versions of the files use different sql_modes
function setSqlMode($strict = true)
```
### DeleteUpgrade

```php
// Delete the damn thing!
function DeleteUpgrade()
```
### cli_scheduled_fetchSMfiles

```php
// Just like the built in one, but setup for CLI to not use themes.
function cli_scheduled_fetchSMfiles()
```
### convertSettingsToTheme

```php
function convertSettingsToTheme()
```
### convertSettingstoOptions

```php
// This function only works with MySQL but that's fine as it is only used for v1.0.
function convertSettingstoOptions()
```
### php_version_check

```php
function php_version_check()
```
### db_version_check

```php
function db_version_check()
```
### fixRelativePath

```php
function fixRelativePath($path)
```
### parse_sql

```php
function parse_sql($filename)
```
### upgrade_query

```php
function upgrade_query($string, $unbuffered = false)
```
### protected_alter

```php
// This performs a table alter, but does it unbuffered so the script can time out professionally.
function protected_alter($change, $substep, $is_test = false)
```
### textfield_alter

```php
function textfield_alter(array $change, int $substep): void
```
Alter a text column definition preserving its character set.



Type|Parameter|Description
---|---|---
`array`|`$change`|
`int`|`$substep`|

### nextSubstep

```php
// The next substep.
function nextSubstep($substep)
```
### cmdStep0

```php
function cmdStep0()
```
### ConvertUtf8

```php
function ConvertUtf8(): void
```
Handles converting your database to UTF-8



### upgrade_unserialize

```php
function upgrade_unserialize(string $string): string|bool
```
Wrapper for unserialize that attempts to repair corrupted serialized data strings



Type|Parameter|Description
---|---|---
`string`|`$string`|Serialized data that may or may not have been corrupted

### serialize_to_json

```php
function serialize_to_json()
```
### template_chmod

```php
/* ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
						Templates are below this point
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~ */
// This is what is displayed if there's any chmod to be done. If not it returns nothing...
function template_chmod()
```
### template_upgrade_above

```php
function template_upgrade_above()
```
### template_upgrade_below

```php
function template_upgrade_below()
```
### template_xml_above

```php
function template_xml_above()
```
### template_xml_below

```php
function template_xml_below()
```
### template_error_message

```php
function template_error_message()
```
### template_welcome_message

```php
function template_welcome_message()
```
### template_upgrade_options

```php
function template_upgrade_options()
```
### template_backup_database

```php
// Template for the database backup tool/
function template_backup_database()
```
### template_backup_xml

```php
function template_backup_xml()
```
### template_database_changes

```php
// Here is the actual "make the changes" template!
function template_database_changes()
```
### template_database_xml

```php
function template_database_xml()
```
### template_convert_utf8

```php
// Template for the UTF-8 conversion step. Basically a copy of the backup stuff with slight modifications....
function template_convert_utf8()
```
### template_convert_xml

```php
function template_convert_xml()
```
### template_serialize_json

```php
// Template for the database backup tool/
function template_serialize_json()
```
### template_serialize_json_xml

```php
function template_serialize_json_xml()
```
### template_upgrade_complete

```php
function template_upgrade_complete()
```
### MySQLConvertOldIp

```php
function MySQLConvertOldIp(string $targetTable, string $oldCol, string $newCol, int $limit = 50000, int $setSize = 100): bool
```
Convert MySQL (var)char ip col to binary

newCol needs to be a varbinary(16) null able field

Type|Parameter|Description
---|---|---
`string`|`$targetTable`|The table to perform the operation on
`string`|`$oldCol`|The old column to gather data from
`string`|`$newCol`|The new column to put data in
`int`|`$limit`|The amount of entries to handle at once\.
`int`|`$setSize`|The amount of entries after which to update the database\.

### upgradeGetColumnInfo

```php
function upgradeGetColumnInfo(string $targetTable, string $column): array
```
Get the column info. This is basically the same as smf_db_list_columns but we get 1 column, force detail and other checks.



Type|Parameter|Description
---|---|---
`string`|`$targetTable`|The table to perform the operation on
`string`|`$column`|The column we are looking for\.

