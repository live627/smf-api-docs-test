---
layout: default
group: func
navtitle: ManageBans.php
title: ./Sources/ManageBans.php
count: 32
---
* auto-gen TOC:
{:toc}
### Ban

```php
function Ban()
```
Ban center. The main entrance point for all ban center functions.

It is accesssed by ?action=admin;area=ban.
It choses a function based on the 'sa' parameter, like many others.
The default sub-action is BanList().
It requires the ban_members permission.
It initializes the admin tabs.

Uses ManageBans template.

### BanList

```php
function BanList()
```
Shows a list of bans currently set.

It is accessed by ?action=admin;area=ban;sa=list.
It removes expired bans.
It allows sorting on different criteria.
It also handles removal of selected ban items.

Uses the main ManageBans template.

### list_getBans

```php
function list_getBans($start, $items_per_page, $sort)
```
Get bans, what else? For the given options.



Type|Parameter|Description
---|---|---
`int`|`$start`|Which item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string telling ORDER BY how to sort the results

### list_getNumBans

```php
function list_getNumBans()
```
Get the total number of ban from the ban group table



### BanEdit

```php
function BanEdit()
```
This function is behind the screen for adding new bans and modifying existing ones.

Adding new bans:
	- is accessed by ?action=admin;area=ban;sa=add.
	- uses the ban_edit sub template of the ManageBans template.
Modifying existing bans:
 - is accessed by ?action=admin;area=ban;sa=edit;bg=x
 - uses the ban_edit sub template of the ManageBans template.
 - shows a list of ban triggers for the specified ban.

### list_getBanItems

```php
function list_getBanItems($start = 0, $items_per_page = 0, $sort = 0, $ban_group_id = 0)
```
Retrieves all the ban items belonging to a certain ban group



Type|Parameter|Description
---|---|---
`int`|`$start`|Which item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`int`|`$sort`|Not used here
`int`|`$ban_group_id`|The ID of the group to get the bans for

### list_getNumBanItems

```php
function list_getNumBanItems()
```
Gets the number of ban items belonging to a certain ban group



### banLoadAdditionalIPs

```php
function banLoadAdditionalIPs($member_id)
```
Finds additional IPs related to a certain user



Type|Parameter|Description
---|---|---
`int`|`$member_id`|The ID of the member to get additional IPs for

### banLoadAdditionalIPsMember

```php
function banLoadAdditionalIPsMember($member_id)
```
Loads additional IPs used by a specific member



Type|Parameter|Description
---|---|---
`int`|`$member_id`|The ID of the member

### banLoadAdditionalIPsError

```php
function banLoadAdditionalIPsError($member_id)
```
Loads additional IPs used by a member from the error log



Type|Parameter|Description
---|---|---
`int`|`$member_id`|The ID of the member

### banEdit2

```php
function banEdit2()
```
This function handles submitted forms that add, modify or remove ban triggers.



### saveTriggers

```php
function saveTriggers(array $suggestions, $ban_group, $member = 0, $ban_id = 0)
```
Saves one or more ban triggers into a ban item: according to the suggestions
checks the $_POST variable to verify if the trigger is present



Type|Parameter|Description
---|---|---
`array`|`$suggestions`|An array of suggestedtriggers (IP, email, etc.)
`int`|`$ban_group`|The ID of the group we're saving bans for
`int`|`$member`|The ID of the member associated with this ban (if applicable)
`int`|`$ban_id`|The ID of the ban (0 if this is a new ban)

### removeBanTriggers

```php
function removeBanTriggers($items_ids = array(), $group_id = false)
```
This function removes a bunch of triggers based on ids
Doesn't clean the inputs



Type|Parameter|Description
---|---|---
`array`|`$items_ids`|The items to remove
`bool&#124;int`|`$group_id`|The ID of the group these triggers are associated with or false if deleting them from all groups

### removeBanGroups

```php
function removeBanGroups($group_ids)
```
This function removes a bunch of ban groups based on ids
Doesn't clean the inputs



Type|Parameter|Description
---|---|---
`int[]`|`$group_ids`|The IDs of the groups to remove

### removeBanLogs

```php
function removeBanLogs($ids = array())
```
Removes logs - by default truncate the table
Doesn't clean the inputs



Type|Parameter|Description
---|---|---
`array`|`$ids`|Empty array to clear the ban log or the IDs of the log entries to remove

### validateTriggers

```php
function validateTriggers(&$triggers)
```
This function validates the ban triggers

Errors in $context['ban_errors']

Type|Parameter|Description
---|---|---
`array`|`$triggers`|The triggers to validate

### addTriggers

```php
function addTriggers($group_id = 0, $triggers = array(), $logs = array())
```
This function actually inserts the ban triggers into the database

Errors in $context['ban_errors']

Type|Parameter|Description
---|---|---
`int`|`$group_id`|The ID of the group to add the triggers to (0 to create a new one)
`array`|`$triggers`|The triggers to add
`array`|`$logs`|The log data

### updateTriggers

```php
function updateTriggers($ban_item = 0, $group_id = 0, $trigger = array(), $logs = array())
```
This function updates an existing ban trigger into the database

Errors in $context['ban_errors']

Type|Parameter|Description
---|---|---
`int`|`$ban_item`|The ID of the ban item
`int`|`$group_id`|The ID of the ban group
`array`|`$trigger`|An array of triggers
`array`|`$logs`|An array of log info

### logTriggersUpdates

```php
function logTriggersUpdates($logs, $new = true, $removal = false)
```
A small function to unify logging of triggers (updates and new)



Type|Parameter|Description
---|---|---
`array`|`$logs`|an array of logs, each log contains the following keys:
- bantype: a known type of ban (ip_range, hostname, email, user, main_ip)
- value: the value of the bantype (e.g. the IP or the email address banned)
`bool`|`$new`|Whether the trigger is new or an update of an existing one
`bool`|`$removal`|Whether the trigger is being deleted

### updateBanGroup

```php
function updateBanGroup($ban_info = array())
```
Updates an existing ban group

Errors in $context['ban_errors']

Type|Parameter|Description
---|---|---
`array`|`$ban_info`|An array of info about the ban group. Should have name and may also have an id.

### insertBanGroup

```php
function insertBanGroup($ban_info = array())
```
Creates a new ban group
If the group is successfully created the ID is returned
On error the error code is returned or false

Errors in $context['ban_errors']

Type|Parameter|Description
---|---|---
`array`|`$ban_info`|An array containing 'name', which is the name of the ban group

### BanEditTrigger

```php
function BanEditTrigger()
```
This function handles the ins and outs of the screen for adding new ban
triggers or modifying existing ones.

Adding new ban triggers:
	- is accessed by ?action=admin;area=ban;sa=edittrigger;bg=x
	- uses the ban_edit_trigger sub template of ManageBans.
Editing existing ban triggers:
 - is accessed by ?action=admin;area=ban;sa=edittrigger;bg=x;bi=y
 - uses the ban_edit_trigger sub template of ManageBans.

### BanBrowseTriggers

```php
function BanBrowseTriggers()
```
This handles the screen for showing the banned entities
It is accessed by ?action=admin;area=ban;sa=browse
It uses sub-tabs for browsing by IP, hostname, email or username.

Uses a standard list (@see createList())

### list_getBanTriggers

```php
function list_getBanTriggers($start, $items_per_page, $sort, $trigger_type)
```
Get ban triggers for the given parameters. Callback from $listOptions['get_items'] in BanBrowseTriggers()



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string telling ORDER BY how to sort the results
`string`|`$trigger_type`|The trigger type - can be 'ip', 'hostname' or 'email'

### list_getNumBanTriggers

```php
function list_getNumBanTriggers($trigger_type)
```
This returns the total number of ban triggers of the given type. Callback for $listOptions['get_count'] in BanBrowseTriggers().



Type|Parameter|Description
---|---|---
`string`|`$trigger_type`|The trigger type. Can be 'ip', 'hostname' or 'email'

### BanLog

```php
function BanLog()
```
This handles the listing of ban log entries, and allows their deletion.

Shows a list of logged access attempts by banned users.
It is accessed by ?action=admin;area=ban;sa=log.
How it works:
 - allows sorting of several columns.
 - also handles deletion of (a selection of) log entries.

### list_getBanLogEntries

```php
function list_getBanLogEntries($start, $items_per_page, $sort)
```
Load a list of ban log entries from the database.

(no permissions check). Callback for $listOptions['get_items'] in BanLog()

Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string telling ORDER BY how to sort the results

### list_getNumBanLogEntries

```php
function list_getNumBanLogEntries()
```
This returns the total count of ban log entries. Callback for $listOptions['get_count'] in BanLog().



### range2ip

```php
function range2ip($low, $high)
```
Convert a range of given IP number into a single string.

It's practically the reverse function of ip2range().

Type|Parameter|Description
---|---|---
`array`|`$low`|The low end of the range in IPv4 format
`array`|`$high`|The high end of the range in IPv4 format

### checkExistingTriggerIP

```php
function checkExistingTriggerIP($ip_array, $fullip = '')
```
Checks whether a given IP range already exists in the trigger list.

If yes, it returns an error message. Otherwise, it returns an array
optimized for the database.

Type|Parameter|Description
---|---|---
`array`|`$ip_array`|An array of IP trigger data
`string`|`$fullip`|The full IP

### updateBanMembers

```php
function updateBanMembers()
```
As it says... this tries to review the list of banned members, to match new bans.

Note: is_activated >= 10: a member is banned.

### getMemberData

```php
function getMemberData($id)
```
Gets basic member data for the ban



Type|Parameter|Description
---|---|---
`int`|`$id`|The ID of the member to get data for

