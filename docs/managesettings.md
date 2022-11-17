---
layout: default
group: func
navtitle: ManageSettings.php
title: ./Sources/ManageSettings.php
count: 20
---
* auto-gen TOC:
{:toc}
### loadGeneralSettingParameters

```php
function loadGeneralSettingParameters(array $subActions = array(), string $defaultAction = null): void
```
This function makes sure the requested subaction does exists, if it doesn't, it sets a default action or.



Type|Parameter|Description
---|---|---
`array`|`$subActions`|An array containing all possible subactions.
`string`|`$defaultAction`|The default action to be called if no valid subaction was found.

### ModifyFeatureSettings

```php
function ModifyFeatureSettings(): void
```
This function passes control through to the relevant tab.



Integration hooks
: integrate_modify_features

### ModifyModSettings

```php
function ModifyModSettings(): void
```
This my friend, is for all the mod authors out there.



Integration hooks
: integrate_modify_modifications

### ModifyBasicSettings

```php
function ModifyBasicSettings(bool $return_config = false): void|array
```
Config array for changing the basic forum settings
Accessed  from ?action=admin;area=featuresettings;sa=basic;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_modify_basic_settings
: integrate_save_basic_settings

### ModifyBBCSettings

```php
function ModifyBBCSettings(bool $return_config = false): void|array
```
Set a few Bulletin Board Code settings. It loads a list of Bulletin Board Code tags to allow disabling tags.

Requires the admin_forum permission.
Accessed from ?action=admin;area=featuresettings;sa=bbc.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_modify_bbc_settings
: integrate_save_bbc_settings

### ModifyLayoutSettings

```php
function ModifyLayoutSettings(bool $return_config = false): void|array
```
Allows modifying the global layout settings in the forum
Accessed through ?action=admin;area=featuresettings;sa=layout;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_layout_settings
: integrate_save_layout_settings

### ModifyLikesSettings

```php
function ModifyLikesSettings(bool $return_config = false): void|array
```
Config array for changing like settings
Accessed  from ?action=admin;area=featuresettings;sa=likes;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array

Integration hooks
: integrate_likes_settings
: integrate_save_likes_settings

### ModifyMentionsSettings

```php
function ModifyMentionsSettings(bool $return_config = false): void|array
```
Config array for changing like settings
Accessed  from ?action=admin;area=featuresettings;sa=mentions;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_mentions_settings
: integrate_save_mentions_settings

### ModifyWarningSettings

```php
function ModifyWarningSettings(bool $return_config = false): void|array
```
Moderation type settings - although there are fewer than we have you believe ;)



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_warning_settings
: integrate_save_warning_settings

### ModifyAntispamSettings

```php
function ModifyAntispamSettings(bool $return_config = false): void|array
```
Let's try keep the spam to a minimum ah Thantos?



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_spam_settings
: integrate_save_spam_settings

### ModifySignatureSettings

```php
function ModifySignatureSettings(bool $return_config = false): void|array
```
You'll never guess what this function does.

..

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_signature_settings
: integrate_apply_signature_settings
: integrate_save_signature_settings

### pauseSignatureApplySettings

```php
function pauseSignatureApplySettings(): void
```
Just pause the signature applying thing.



### ShowCustomProfiles

```php
function ShowCustomProfiles(): void
```
Show all the custom profile fields available to the user.



### list_getProfileFields

```php
function list_getProfileFields(int $start, int $items_per_page, string $sort, bool $standardFields): array
```
Callback for createList().



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (used for pagination purposes)
`int`|`$items_per_page`|The number of items to display per page
`string`|`$sort`|A string indicating how to sort the results
`bool`|`$standardFields`|Whether or not to include standard fields as well

### list_getProfileFieldSize

```php
function list_getProfileFieldSize(): int
```
Callback for createList().



### EditCustomProfiles

```php
function EditCustomProfiles(): void
```
Edit some profile fields?



### custFieldsMaxOrder

```php
function custFieldsMaxOrder(): int
```
Returns the maximum field_order value for the custom fields



### ModifyLogSettings

```php
function ModifyLogSettings(bool $return_config = false): void|array
```
Allow to edit the settings on the pruning screen.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_prune_settings
: integrate_prune_settings

### ModifyGeneralModSettings

```php
function ModifyGeneralModSettings(bool $return_config = false): void|array
```
If you have a general mod setting to add stick it here.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_general_mod_settings
: integrate_save_general_mod_settings

### ModifyAlertsSettings

```php
function ModifyAlertsSettings(): void
```
Handles modifying the alerts settings



