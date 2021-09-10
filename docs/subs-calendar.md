---
layout: default
group: func
navtitle: Subs-Calendar.php
title: ./Sources/Subs-Calendar.php
count: 26
---
* auto-gen TOC:
{:toc}
### getBirthdayRange

```php
function getBirthdayRange($low_date, $high_date)
```
Get all birthdays within the given time range.

finds all the birthdays in the specified range of days.
works with birthdays set for no year, or any other year, and respects month and year boundaries.

Type|Parameter|Description
---|---|---
`string`|`$low_date`|The low end of the range, inclusive, in YYYY-MM-DD format
`string`|`$high_date`|The high end of the range, inclusive, in YYYY-MM-DD format

### getEventRange

```php
function getEventRange($low_date, $high_date, $use_permissions = true)
```
Get all calendar events within the given time range.

- finds all the posted calendar events within a date range.
- both the earliest_date and latest_date should be in the standard YYYY-MM-DD format.
- censors the posted event titles.
- uses the current user's permissions if use_permissions is true, otherwise it does nothing "permission specific"

Type|Parameter|Description
---|---|---
`string`|`$low_date`|The low end of the range, inclusive, in YYYY-MM-DD format
`string`|`$high_date`|The high end of the range, inclusive, in YYYY-MM-DD format
`bool`|`$use_permissions`|Whether to use permissions

### getHolidayRange

```php
function getHolidayRange($low_date, $high_date)
```
Get all holidays within the given time range.



Type|Parameter|Description
---|---|---
`string`|`$low_date`|The low end of the range, inclusive, in YYYY-MM-DD format
`string`|`$high_date`|The high end of the range, inclusive, in YYYY-MM-DD format

### canLinkEvent

```php
function canLinkEvent()
```
Does permission checks to see if an event can be linked to a board/topic.

checks if the current user can link the current topic to the calendar, permissions et al.
this requires the calendar_post permission, a forum moderator, or a topic starter.
expects the $topic and $board variables to be set.
if the user doesn't have proper permissions, an error will be shown.

### getTodayInfo

```php
function getTodayInfo()
```
Returns date information about 'today' relative to the users time offset.

returns an array with the current date, day, month, and year.
takes the users time offset into account.

### getCalendarGrid

```php
function getCalendarGrid($selected_date, $calendarOptions, $is_previous = false, $has_picker = true)
```
Provides information (link, month, year) about the previous and next month.



Type|Parameter|Description
---|---|---
`string`|`$selected_date`|A date in YYYY-MM-DD format
`array`|`$calendarOptions`|An array of calendar options
`bool`|`$is_previous`|Whether this is the previous month
`bool`|`$has_picker`|Wheter to add javascript to handle a date picker

### getCalendarWeek

```php
function getCalendarWeek($selected_date, $calendarOptions)
```
Returns the information needed to show a calendar for the given week.



Type|Parameter|Description
---|---|---
`string`|`$selected_date`|A date in YYYY-MM-DD format
`array`|`$calendarOptions`|An array of calendar options

### getCalendarList

```php
function getCalendarList($start_date, $end_date, $calendarOptions)
```
Returns the information needed to show a list of upcoming events, birthdays, and holidays on the calendar.



Type|Parameter|Description
---|---|---
`string`|`$start_date`|The start of a date range in YYYY-MM-DD format
`string`|`$end_date`|The end of a date range in YYYY-MM-DD format
`array`|`$calendarOptions`|An array of calendar options

### loadDatePicker

```php
function loadDatePicker($selector = 'input.date_input', $date_format = '')
```
Loads the necessary JavaScript and CSS to create a datepicker.



Type|Parameter|Description
---|---|---
`string`|`$selector`|A CSS selector for the input field(s) that the datepicker should be attached to.
`string`|`$date_format`|The date format to use, in strftime() format.

### loadTimePicker

```php
function loadTimePicker($selector = 'input.time_input', $time_format = '')
```
Loads the necessary JavaScript and CSS to create a timepicker.



Type|Parameter|Description
---|---|---
`string`|`$selector`|A CSS selector for the input field(s) that the timepicker should be attached to.
`string`|`$time_format`|A time format in strftime format

### loadDatePair

```php
function loadDatePair($container, $date_class = '', $time_class = '')
```
Loads the necessary JavaScript for Datepair.js.

Datepair.js helps to keep date ranges sane in the UI.

Type|Parameter|Description
---|---|---
`string`|`$container`|CSS selector for the containing element of the date/time inputs to be paired.
`string`|`$date_class`|The CSS class of the date inputs to be paired.
`string`|`$time_class`|The CSS class of the time inputs to be paired.

### cache_getOffsetIndependentEvents

```php
function cache_getOffsetIndependentEvents($eventOptions)
```
Retrieve all events for the given days, independently of the users offset.

cache callback function used to retrieve the birthdays, holidays, and events between now and now + days_to_index.
widens the search range by an extra 24 hours to support time offset shifts.
used by the cache_getRecentEvents function to get the information needed to calculate the events taking the users time offset into account.

Type|Parameter|Description
---|---|---
`array`|`$eventOptions`|With the keys 'num_days_shown', 'include_holidays', 'include_birthdays' and 'include_events'

### cache_getRecentEvents

```php
function cache_getRecentEvents($eventOptions)
```
cache callback function used to retrieve the upcoming birthdays, holidays, and events within the given period, taking into account the users time offset.

Called from the BoardIndex to display the current day's events on the board index
used by the board index and SSI to show the upcoming events.

Type|Parameter|Description
---|---|---
`array`|`$eventOptions`|An array of event options.

### validateEventPost

```php
function validateEventPost()
```
Makes sure the calendar post is valid.



### getEventPoster

```php
function getEventPoster($event_id)
```
Get the event's poster.



Type|Parameter|Description
---|---|---
`int`|`$event_id`|The ID of the event

### insertEvent

```php
function insertEvent(&$eventOptions)
```
Consolidating the various INSERT statements into this function.

Inserts the passed event information into the calendar table.
Allows to either set a time span (in days) or an end_date.
Does not check any permissions of any sort.

Type|Parameter|Description
---|---|---
`array`|`$eventOptions`|An array of event options ('title', 'span', 'start_date', 'end_date', etc.)

### modifyEvent

```php
function modifyEvent($event_id, &$eventOptions)
```
modifies an event.

allows to either set a time span (in days) or an end_date.
does not check any permissions of any sort.

Type|Parameter|Description
---|---|---
`int`|`$event_id`|The ID of the event
`array`|`$eventOptions`|An array of event information

### removeEvent

```php
function removeEvent($event_id)
```
Remove an event
removes an event.

does no permission checks.

Type|Parameter|Description
---|---|---
`int`|`$event_id`|The ID of the event to remove

### getEventProperties

```php
function getEventProperties($event_id)
```
Gets all the events properties



Type|Parameter|Description
---|---|---
`int`|`$event_id`|The ID of the event

### getNewEventDatetimes

```php
function getNewEventDatetimes()
```
Gets an initial set of date and time values for creating a new event.



### setEventStartEnd

```php
function setEventStartEnd($eventOptions = array())
```
Set the start and end dates and times for a posted event for insertion into the database.

Validates all date and times given to it.
Makes sure events do not exceed the maximum allowed duration (if any).
If passed an array that defines any time or date parameters, they will be used. Otherwise, gets the values from $_POST.

Type|Parameter|Description
---|---|---
`array`|`$eventOptions`|An array of optional time and date parameters (span, start_year, end_month, etc., etc.)

### buildEventDatetimes

```php
function buildEventDatetimes($row)
```
Helper function for getEventRange, getEventProperties, getNewEventDatetimes, etc.



Type|Parameter|Description
---|---|---
`array`|`$row`|A database row representing an event from the calendar table

### list_getHolidays

```php
function list_getHolidays($start, $items_per_page, $sort)
```
Gets all of the holidays for the listing



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string indicating how to sort the results

### list_getNumHolidays

```php
function list_getNumHolidays()
```
Helper function to get the total number of holidays



### removeHolidays

```php
function removeHolidays($holiday_ids)
```
Remove a holiday from the calendar



Type|Parameter|Description
---|---|---
`array`|`$holiday_ids`|An array of IDs of holidays to delete

### convertDateToEnglish

```php
function convertDateToEnglish($date)
```
Helper function to convert date string to english
so that date_parse can parse the date



Type|Parameter|Description
---|---|---
`string`|`$date`|A localized date string

