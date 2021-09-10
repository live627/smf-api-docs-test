---
layout: default
group: func
navtitle: ManageCalendar.php
title: ./Sources/ManageCalendar.php
count: 4
---
* auto-gen TOC:
{:toc}
### ManageCalendar

```php
function ManageCalendar()
```
The main controlling function doesn't have much to do... yet.

Just check permissions and delegate to the rest.

Uses ManageCalendar language file.

### ModifyHolidays

```php
function ModifyHolidays()
```
The function that handles adding, and deleting holiday data



### EditHoliday

```php
function EditHoliday()
```
This function is used for adding/editing a specific holiday



### ModifyCalendarSettings

```php
function ModifyCalendarSettings($return_config = false)
```
Show and allow to modify calendar settings. Obviously.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config_vars array (used for admin search)

