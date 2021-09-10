---
layout: default
group: func
navtitle: Calendar.template.php
title: ./Themes/default/Calendar.template.php
count: 10
---
* auto-gen TOC:
{:toc}
### template_main

```php
function template_main()
```
Our main calendar template, which encapsulates weeks and months.



### template_show_upcoming_list

```php
function template_show_upcoming_list($grid_name)
```
Display a list of upcoming events, birthdays, and holidays.



Type|Parameter|Description
---|---|---
`string`|`$grid_name`|The grid name

### template_show_month_grid

```php
function template_show_month_grid($grid_name, $is_mini = false)
```
Display a monthly calendar grid.



Type|Parameter|Description
---|---|---
`string`|`$grid_name`|The grid name
`bool`|`$is_mini`|Is this a mini grid?

### template_show_week_grid

```php
function template_show_week_grid($grid_name)
```
Shows a weekly grid



Type|Parameter|Description
---|---|---
`string`|`$grid_name`|The name of the grid

### template_calendar_top

```php
function template_calendar_top($calendar_data)
```
Calendar controls under the title

Creates the view selector (list, month, week), the date selector (either a
select menu or a date range chooser, depending on the circumstances), and the
"Post Event" button.

Type|Parameter|Description
---|---|---
`array`|`$calendar_data`|The data for the calendar grid that this is for

### template_event_post

```php
function template_event_post()
```
Template for posting a calendar event.



### template_bcd

```php
function template_bcd()
```
Displays a clock



### template_hms

```php
function template_hms()
```
Displays the hours, minutes and seconds for our clock



### template_omfg

```php
function template_omfg()
```
Displays a binary clock



### template_thetime

```php
function template_thetime()
```
Displays the time



