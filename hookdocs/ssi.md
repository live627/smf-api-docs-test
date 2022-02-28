---
layout: default
group: hooks
title: SSI.php
count: 20
---
* auto-gen TOC:
{:toc}
### integrate_autoload

```php
call_integration_hook('integrate_autoload', array(&$classMap))
```

Type|Parameter|Description
---|---|---
`array`|`&$classMap`|desc

Called from
: [`()` in `./SSI.php`](../docs/ssi.html#)

Notes
: Since 2.1

### integrate_SSI

```php
call_integration_hook('integrate_SSI')
```


Called from
: [`()` in `./SSI.php`](../docs/ssi.html#)

Notes
: Since 2.1

### integrate_ssi_queryPosts

```php
call_integration_hook('integrate_ssi_queryPosts', array(&$posts))
```

Type|Parameter|Description
---|---|---
`array`|`&$posts`|desc

Called from
: [`ssi_queryPosts()` in `./SSI.php`](../docs/ssi.html#ssi_queryposts)

Notes
: Since 2.1

### integrate_ssi_recentTopics

```php
call_integration_hook('integrate_ssi_recentTopics', array(&$posts))
```

Type|Parameter|Description
---|---|---
`array`|`&$posts`|desc

Called from
: [`ssi_recentTopics()` in `./SSI.php`](../docs/ssi.html#ssi_recenttopics)

Notes
: Since 2.1

### integrate_ssi_topPoster

```php
call_integration_hook('integrate_ssi_topPoster', array(&$return))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

Called from
: [`ssi_topPoster()` in `./SSI.php`](../docs/ssi.html#ssi_topposter)

Notes
: Since 2.1

### integrate_ssi_topBoards

```php
call_integration_hook('integrate_ssi_topBoards', array(&$boards))
```

Type|Parameter|Description
---|---|---
`array`|`&$boards`|desc

Called from
: [`ssi_topBoards()` in `./SSI.php`](../docs/ssi.html#ssi_topboards)

Notes
: Since 2.1

### integrate_ssi_topTopics

```php
call_integration_hook('integrate_ssi_topTopics', array(&$topics, $type))
```

Type|Parameter|Description
---|---|---
`array`|`&$topics`|desc
`array`|`$type`|desc

Called from
: [`ssi_topTopics()` in `./SSI.php`](../docs/ssi.html#ssi_toptopics)

Notes
: Since 2.1

### integrate_ssi_queryMembers

```php
call_integration_hook('integrate_ssi_queryMembers', array(&$members))
```

Type|Parameter|Description
---|---|---
`array`|`&$members`|desc

Called from
: [`ssi_queryMembers()` in `./SSI.php`](../docs/ssi.html#ssi_querymembers)

Notes
: Since 2.1

### integrate_ssi_boardStats

```php
call_integration_hook('integrate_ssi_boardStats', array(&$totals))
```

Type|Parameter|Description
---|---|---
`array`|`&$totals`|desc

Called from
: [`ssi_boardStats()` in `./SSI.php`](../docs/ssi.html#ssi_boardstats)

Notes
: Since 2.1

### integrate_ssi_whosOnline

```php
call_integration_hook('integrate_ssi_whosOnline', array(&$return))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

Called from
: [`ssi_whosOnline()` in `./SSI.php`](../docs/ssi.html#ssi_whosonline)

Notes
: Since 2.1

### integrate_ssi_recentPoll

```php
call_integration_hook('integrate_ssi_recentPoll', array(&$return, $topPollInstead))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc
`array`|`$topPollInstead`|desc

Called from
: [`ssi_recentPoll()` in `./SSI.php`](../docs/ssi.html#ssi_recentpoll)

Notes
: Since 2.1

### integrate_ssi_showPoll

```php
call_integration_hook('integrate_ssi_showPoll', array(&$return))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

Called from
: [`ssi_showPoll()` in `./SSI.php`](../docs/ssi.html#ssi_showpoll)

Notes
: Since 2.1

### integrate_ssi_news

```php
call_integration_hook('integrate_ssi_news')
```


Called from
: [`ssi_news()` in `./SSI.php`](../docs/ssi.html#ssi_news)

Notes
: Since 2.1

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc
`array`|`$eventOptions`|desc

Called from
: [`ssi_todaysBirthdays()` in `./SSI.php`](../docs/ssi.html#ssi_todaysbirthdays)

Notes
: Since 2.1

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc
`array`|`$eventOptions`|desc

Called from
: [`ssi_todaysHolidays()` in `./SSI.php`](../docs/ssi.html#ssi_todaysholidays)

Notes
: Since 2.1

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc
`array`|`$eventOptions`|desc

Called from
: [`ssi_todaysEvents()` in `./SSI.php`](../docs/ssi.html#ssi_todaysevents)

Notes
: Since 2.1

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc
`array`|`$eventOptions`|desc

Called from
: [`ssi_todaysCalendar()` in `./SSI.php`](../docs/ssi.html#ssi_todayscalendar)

Notes
: Since 2.1

### integrate_ssi_boardNews

```php
call_integration_hook('integrate_ssi_boardNews', array(&$return))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

Called from
: [`ssi_boardNews()` in `./SSI.php`](../docs/ssi.html#ssi_boardnews)

Notes
: Since 2.1

### integrate_ssi_recentEvents

```php
call_integration_hook('integrate_ssi_recentEvents', array(&$return))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

Called from
: [`ssi_recentEvents()` in `./SSI.php`](../docs/ssi.html#ssi_recentevents)

Notes
: Since 2.1

### integrate_ssi_recentAttachments

```php
call_integration_hook('integrate_ssi_recentAttachments', array(&$attachments))
```

Type|Parameter|Description
---|---|---
`array`|`&$attachments`|desc

Called from
: [`ssi_recentAttachments()` in `./SSI.php`](../docs/ssi.html#ssi_recentattachments)

Notes
: Since 2.1

