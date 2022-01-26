---
layout: default
group: func
navtitle: Calendar.php
title: ./Sources/Calendar.php
count: 4
---
* auto-gen TOC:
{:toc}
### CalendarMain

```php
function CalendarMain(): void
```
Show the calendar.

It loads the specified month's events, holidays, and birthdays.
It requires the calendar_view permission.
It depends on the cal_enabled setting, and many of the other cal_ settings.
It uses the calendar_start_day theme option. (Monday/Sunday)
It uses the main sub template in the Calendar template.
It goes to the month and year passed in 'month' and 'year' by get or post.
It is accessed through ?action=calendar.

### CalendarPost

```php
function CalendarPost(): void
```
This function processes posting/editing/deleting a calendar event.

- calls {@link Post.php|Post() Post()} function if event is linked to a post.
 - calls {@link Subs-Calendar.php|insertEvent() insertEvent()} to insert the event if not linked to post.

It requires the calendar_post permission to use.
It uses the event_post sub template in the Calendar template.
It is accessed with ?action=calendar;sa=post.

### iCalDownload

```php
function iCalDownload(): void
```
This function offers up a download of an event in iCal 2.0 format.

Follows the conventions in {@link https://tools.ietf.org/html/rfc5546 RFC5546}
Sets events as all day events since we don't have hourly events
Will honor and set multi day events
Sets a sequence number if the event has been modified

### clock

```php
function clock(): void
```
Nothing to see here. Move along.



