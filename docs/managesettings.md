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
function loadGeneralSettingParameters($subActions = array(), $defaultAction = null)
```
This function makes sure the requested subaction does exists, if it doesn't, it sets a default action or.



Type|Parameter|Description
---|---|---
`array`|`$subActions`|An array containing all possible subactions.
`string`|`$defaultAction`|The default action to be called if no valid subaction was found.

### ModifyFeatureSettings

```php
function ModifyFeatureSettings()
```
This function passes control through to the relevant tab.



### ModifyModSettings

```php
function ModifyModSettings()
```
This my friend, is for all the mod authors out there.



### ModifyBasicSettings

```php
function ModifyBasicSettings($return_config = false)
```
Config array for changing the basic forum settings
Accessed  from ?action=admin;area=featuresettings;sa=basic;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyBBCSettings

```php
function ModifyBBCSettings($return_config = false)
```
Set a few Bulletin Board Code settings. It loads a list of Bulletin Board Code tags to allow disabling tags.

Requires the admin_forum permission.
Accessed from ?action=admin;area=featuresettings;sa=bbc.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyLayoutSettings

```php
function ModifyLayoutSettings($return_config = false)
```
Allows modifying the global layout settings in the forum
Accessed through ?action=admin;area=featuresettings;sa=layout;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyLikesSettings

```php
function ModifyLikesSettings($return_config = false)
```
Config array for changing like settings
Accessed  from ?action=admin;area=featuresettings;sa=likes;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array

### ModifyMentionsSettings

```php
function ModifyMentionsSettings($return_config = false)
```
Config array for changing like settings
Accessed  from ?action=admin;area=featuresettings;sa=mentions;



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyWarningSettings

```php
function ModifyWarningSettings($return_config = false)
```
Moderation type settings - although there are fewer than we have you believe ;)



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyAntispamSettings

```php
function ModifyAntispamSettings($return_config = false)
```
Let's try keep the spam to a minimum ah Thantos?



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifySignatureSettings

```php
function ModifySignatureSettings($return_config = false)
```
You'll never guess what this function does.

..

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### pauseSignatureApplySettings

```php
function pauseSignatureApplySettings()
```
Just pause the signature applying thing.



### ShowCustomProfiles

```php
function ShowCustomProfiles()
```
Show all the custom profile fields available to the user.



### list_getProfileFields

```php
function list_getProfileFields($start, $items_per_page, $sort, $standardFields)
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
function list_getProfileFieldSize()
```
Callback for createList().



### EditCustomProfiles

```php
function EditCustomProfiles()
```
Edit some profile fields?



### custFieldsMaxOrder

```php
function custFieldsMaxOrder()
```
Returns the maximum field_order value for the custom fields



### ModifyLogSettings

```php
function ModifyLogSettings($return_config = false)
```
Allow to edit the settings on the pruning screen.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyGeneralModSettings

```php
function ModifyGeneralModSettings($return_config = false)
```
If you have a general mod setting to add stick it here.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyAlertsSettings

```php
function ModifyAlertsSettings()
```
Handles modifying the alerts settings



