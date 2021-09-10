---
layout: default
group: func
navtitle: Subs-Notify.php
title: ./Sources/Subs-Notify.php
count: 5
---
* auto-gen TOC:
{:toc}
### getNotifyPrefs

```php
function getNotifyPrefs($members, $prefs = '', $process_default = false)
```
Fetches the list of preferences (or a single/subset of preferences) for
notifications for one or more users.



Type|Parameter|Description
---|---|---
`int&#124;array`|`$members`|A user id or an array of (integer) user ids to load preferences for
`string&#124;array`|`$prefs`|An empty string to load all preferences, or a string (or array) of preference name(s) to load
`bool`|`$process_default`|Whether to apply the default values to the members' values or not.

### setNotifyPrefs

```php
function setNotifyPrefs($memID, $prefs = array())
```
Sets the list of preferences for a single user.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The user whose preferences you are setting
`array`|`$prefs`|An array key of pref -> value

### deleteNotifyPrefs

```php
function deleteNotifyPrefs($memID, array $prefs)
```
Deletes notification preference



Type|Parameter|Description
---|---|---
`int`|`$memID`|The user whose preference you're setting
`array`|`$prefs`|The preferences to delete

### getMemberWithToken

```php
function getMemberWithToken($type)
```
Verifies a member's unsubscribe token, then returns some member info



Type|Parameter|Description
---|---|---
`string`|`$type`|The type of notification the token is for (e.g. 'board', 'topic', etc.)

### createUnsubscribeToken

```php
function createUnsubscribeToken($memID, $email, $type = '', $itemID = 0)
```
Builds an unsubscribe token



Type|Parameter|Description
---|---|---
`int`|`$memID`|The id of the member that this token is for
`string`|`$email`|The member's email address
`string`|`$type`|The type of notification the token is for (e.g. 'board', 'topic', etc.)
`int`|`$itemID`|The id of the notification item, if applicable.

