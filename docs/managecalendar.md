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
function ManageCalendar(): void
```
The main controlling function doesn't have much to do... yet.

Just check permissions and delegate to the rest.

Uses ManageCalendar language file.

Integration hooks
: integrate_manage_calendar

### ModifyHolidays

```php
function ModifyHolidays(): void
```
The function that handles adding, and deleting holiday data



### EditHoliday

```php
function EditHoliday(): void
```
This function is used for adding/editing a specific holiday



### ModifyCalendarSettings

```php
function ModifyCalendarSettings(bool $return_config = false): void|array
```
Show and allow to modify calendar settings. Obviously.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config\_vars array \(used for admin search\)

Integration hooks
: integrate_modify_calendar_settings
: integrate_save_calendar_settings

