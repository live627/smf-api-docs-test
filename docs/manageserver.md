---
layout: default
group: func
navtitle: ManageServer.php
title: ./Sources/ManageServer.php
count: 17
---
* auto-gen TOC:
{:toc}
### ModifySettings

```php
function ModifySettings(): void
```
This is the main dispatcher. Sets up all the available sub-actions, all the tabs and selects
the appropriate one based on the sub-action.

Requires the admin_forum permission.
Redirects to the appropriate function based on the sub-action.

Uses edit_settings adminIndex.

### ModifyGeneralSettings

```php
function ModifyGeneralSettings(bool $return_config = false): void|array
```
General forum settings - forum name, maintenance mode, etc.

Practically, this shows an interface for the settings in Settings.php to be changed.

- Requires the admin_forum permission.
- Uses the edit_settings administration area.
- Contains the actual array of settings to show from Settings.php.
- Accessed from ?action=admin;area=serversettings;sa=general.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config_vars array (for pagination purposes)

### AlignURLsWithSSLSetting

```php
function AlignURLsWithSSLSetting(int $new_force_ssl = 0): void
```
Align URLs with SSL Setting.

If force_ssl has changed, ensure all URLs are aligned with the new setting.
This includes:
    - $boardurl
    - $modSettings['smileys_url']
    - $modSettings['avatar_url']
    - $modSettings['custom_avatar_url'] - if found
    - theme_url - all entries in the themes table
    - images_url - all entries in the themes table

This function will NOT overwrite URLs that are not subfolders of $boardurl.
The admin must have pointed those somewhere else on purpose, so they must be updated manually.

A word of caution: You can't trust the http/https scheme reflected for these URLs in $globals
(e.g., $boardurl) or in $modSettings.  This is because SMF may change them in memory to comply
with the force_ssl setting - a soft redirect may be in effect...  Thus, conditional updates
to these values do not work.  You gotta just brute force overwrite them based on force_ssl.

Type|Parameter|Description
---|---|---
`int`|`$new_force_ssl`|is the current force_ssl setting.

### BoardurlMatch

```php
function BoardurlMatch(string $url = ''): bool
```
$boardurl Match.

Helper function to see if the url being checked is based off of $boardurl.
If not, it was overridden by the admin to some other value on purpose, and should not
be stepped on by SMF when aligning URLs with the force_ssl setting.
The site admin must change URLs that are not aligned with $boardurl manually.

Type|Parameter|Description
---|---|---
`string`|`$url`|is the url to check.

### ModifyDatabaseSettings

```php
function ModifyDatabaseSettings(bool $return_config = false): void|array
```
Basic database and paths settings - database name, host, etc.

- It shows an interface for the settings in Settings.php to be changed.
- It contains the actual array of settings to show from Settings.php.
- Requires the admin_forum permission.
- Uses the edit_settings administration area.
- Accessed from ?action=admin;area=serversettings;sa=database.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyCookieSettings

```php
function ModifyCookieSettings(bool $return_config = false): void|array
```
This function handles cookies settings modifications.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyGeneralSecuritySettings

```php
function ModifyGeneralSecuritySettings(bool $return_config = false): void|array
```
Settings really associated with general security aspects.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyCacheSettings

```php
function ModifyCacheSettings(bool $return_config = false): void|array
```
Simply modifying cache functions



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyExportSettings

```php
function ModifyExportSettings(bool $return_config = false): void|array
```
Controls settings for data export functionality



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyLoadBalancingSettings

```php
function ModifyLoadBalancingSettings(bool $return_config = false): void|array
```
Allows to edit load balancing settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array

### prepareServerSettingsContext

```php
function prepareServerSettingsContext(array &$config_vars): void
```
Helper function, it sets up the context for the manage server settings.

- The basic usage of the six numbered key fields are
- array (0 ,1, 2, 3, 4, 5
	0 variable name - the name of the saved variable
	1 label - the text to show on the settings page
	2 saveto - file or db, where to save the variable name - value pair
	3 type - type of data to save, int, float, text, check
	4 size - false or field size
	5 help - '' or helptxt variable name
)

the following named keys are also permitted
'disabled' => A string of code that will determine whether or not the setting should be disabled
'postinput' => Text to display after the input field
'preinput' => Text to display before the input field
'subtext' => Additional descriptive text to display under the field's label
'min' => minimum allowed value (for int/float). Defaults to 0 if not set.
'max' => maximum allowed value (for int/float)
'step' => how much to increment/decrement the value by (only for int/float - mostly used for float values).

Type|Parameter|Description
---|---|---
`array`|`$config_vars`|An array of configuration variables

### prepareDBSettingContext

```php
function prepareDBSettingContext(array &$config_vars): void
```
Helper function, it sets up the context for database settings.



Type|Parameter|Description
---|---|---
`array`|`$config_vars`|An array of configuration variables

### saveSettings

```php
function saveSettings(array &$config_vars): void
```
Helper function. Saves settings by putting them in Settings.php or saving them in the settings table.

- Saves those settings set from ?action=admin;area=serversettings.
- Requires the admin_forum permission.
- Contains arrays of the types of data to save into Settings.php.

Type|Parameter|Description
---|---|---
`array`|`$config_vars`|An array of configuration variables

### saveDBSettings

```php
function saveDBSettings(array &$config_vars): void
```
Helper function for saving database settings.



Type|Parameter|Description
---|---|---
`array`|`$config_vars`|An array of configuration variables

### ShowPHPinfoSettings

```php
function ShowPHPinfoSettings(): void
```
Allows us to see the servers php settings

- loads the settings into an array for display in a template
- drops cookie values just in case

### loadCacheAPIs

```php
function loadCacheAPIs(): void
```
Get the installed Cache API implementations.



### registerSMStats

```php
function registerSMStats(): void
```
Registers the site with the Simple Machines Stat collection. This function
purposely does not use updateSettings.php as it will be called shortly after
this process completes by the saveSettings() function.



