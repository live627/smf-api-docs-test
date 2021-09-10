---
layout: default
group: func
navtitle: ManagePaid.php
title: ./Sources/ManagePaid.php
count: 13
---
* auto-gen TOC:
{:toc}
### ManagePaidSubscriptions

```php
function ManagePaidSubscriptions()
```
The main entrance point for the 'Paid Subscription' screen, calling
the right function based on the given sub-action.

It defaults to sub-action 'view'.
Accessed from ?action=admin;area=paidsubscribe.
It requires admin_forum permission for admin based actions.

### ModifySubscriptionSettings

```php
function ModifySubscriptionSettings($return_config = false)
```
Set any setting related to paid subscriptions, i.e.

modify which payment methods are to be used.
It requires the moderate_forum permission
Accessed from ?action=admin;area=paidsubscribe;sa=settings.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the $config_vars array (used for admin search)

### ViewSubscriptions

```php
function ViewSubscriptions()
```
View a list of all the current subscriptions
Requires the admin_forum permission.

Accessed from ?action=admin;area=paidsubscribe;sa=view.

### ModifySubscription

```php
function ModifySubscription()
```
Adding, editing and deleting subscriptions.

Accessed from ?action=admin;area=paidsubscribe;sa=modify.

### ViewSubscribedUsers

```php
function ViewSubscribedUsers()
```
View all the users subscribed to a particular subscription.

Requires the admin_forum permission.
Accessed from ?action=admin;area=paidsubscribe;sa=viewsub.

Subscription ID is required, in the form of $_GET['sid'].

### list_getSubscribedUserCount

```php
function list_getSubscribedUserCount($id_sub, $search_string, $search_vars = array())
```
Returns how many people are subscribed to a paid subscription.



Type|Parameter|Description
---|---|---
`int`|`$id_sub`|The ID of the subscription
`string`|`$search_string`|A search string
`array`|`$search_vars`|An array of variables for the search string

### list_getSubscribedUsers

```php
function list_getSubscribedUsers($start, $items_per_page, $sort, $id_sub, $search_string, $search_vars = array())
```
Return the subscribed users list, for the given parameters.



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string indicating how to sort the results
`int`|`$id_sub`|The ID of the subscription
`string`|`$search_string`|A search string
`array`|`$search_vars`|The variables for the search string

### ModifyUserSubscription

```php
function ModifyUserSubscription()
```
Edit or add a user subscription.

Accessed from ?action=admin;area=paidsubscribe;sa=modifyuser.

### reapplySubscriptions

```php
function reapplySubscriptions($users)
```
Reapplies all subscription rules for each of the users.



Type|Parameter|Description
---|---|---
`array`|`$users`|An array of user IDs

### addSubscription

```php
function addSubscription($id_subscribe, $id_member, $renewal = 0, $forceStartTime = 0, $forceEndTime = 0)
```
Add or extend a subscription of a user.



Type|Parameter|Description
---|---|---
`int`|`$id_subscribe`|The subscription ID
`int`|`$id_member`|The ID of the member
`int&#124;string`|`$renewal`|0 if we're forcing start/end time, otherwise a string indicating how long to renew the subscription for ('D', 'W', 'M' or 'Y')
`int`|`$forceStartTime`|If set, forces the subscription to start at the specified time
`int`|`$forceEndTime`|If set, forces the subscription to end at the specified time

### removeSubscription

```php
function removeSubscription($id_subscribe, $id_member, $delete = false)
```
Removes a subscription from a user, as in removes the groups.



Type|Parameter|Description
---|---|---
`int`|`$id_subscribe`|The ID of the subscription
`int`|`$id_member`|The ID of the member
`bool`|`$delete`|Whether to delete the subscription or just disable it

### loadSubscriptions

```php
function loadSubscriptions()
```
This just kind of caches all the subscription data.



### loadPaymentGateways

```php
function loadPaymentGateways()
```
Load all the payment gateways.

Checks the Sources directory for any files fitting the format of a payment gateway,
loads each file to check it's valid, includes each file and returns the
function name and whether it should work with this version of SMF.

