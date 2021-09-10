---
layout: default
group: func
navtitle: Profile-Actions.php
title: ./Sources/Profile-Actions.php
count: 7
---
* auto-gen TOC:
{:toc}
### activateAccount

```php
function activateAccount($memID)
```
Activate an account.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member whose account we're activating

### issueWarning

```php
function issueWarning($memID)
```
Issue/manage an user's warning status.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the user

### list_getUserWarningCount

```php
function list_getUserWarningCount($memID)
```
Get the number of warnings a user has. Callback for $listOptions['get_count'] in issueWarning()



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the user

### list_getUserWarnings

```php
function list_getUserWarnings($start, $items_per_page, $sort, $memID)
```
Get the data about a user's warnings. Callback function for the list in issueWarning()



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string indicating how to sort the results
`int`|`$memID`|The member ID

### deleteAccount

```php
function deleteAccount($memID)
```
Present a screen to make sure the user wants to be deleted



Type|Parameter|Description
---|---|---
`int`|`$memID`|The member ID

### deleteAccount2

```php
function deleteAccount2($memID)
```
Actually delete an account.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The member ID

### subscriptions

```php
function subscriptions($memID)
```
Function for doing all the paid subscription stuff - kinda.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the user whose subscriptions we're viewing

