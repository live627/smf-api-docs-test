---
layout: default
group: hooks
title: SSI
---

### integrate_SSI

```php
call_integration_hook('integrate_SSI')
```
A general hook that you can use when SMF is in SSI mode.

### integrate_ssi_queryPosts

```php
call_integration_hook('integrate_ssi_queryPosts', array(&$posts)
```

Type|Parameter|Description
---|---|---
`array`|`&$posts`|Associative array of posts with message ids as keys


Called from
: queryPosts()

### integrate_ssi_recentTopics

```php
call_integration_hook('integrate_ssi_recentTopics', array(&$posts)
```

Type|Parameter|Description
---|---|---
`array`|`&$posts`|List of posts

Called from
: recentTopics()
### integrate_ssi_topPoster

```php
call_integration_hook('integrate_ssi_topPoster', array(&$return)
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|List of members.

Called from
: topPoster()
Notes
: Each element has the following definition:

    Type|Key|Description
    ---|---|---
    `string`|`id`|The member id
    `string`|`name`|The member real name; this is the name that can be changed at will
    `string`|`link`|HTML formatted link to their profile
    `string`|`posts`|Number of posts
: Numeric values are strings because the native mysqld driver only returns strings.
### integrate_ssi_topBoards

```php
call_integration_hook('integrate_ssi_topBoards', array(&$boards)
```

Type|Parameter|Description
---|---|---
`array`|`&$boards`|desc

### integrate_ssi_topTopics

```php
call_integration_hook('integrate_ssi_topTopics', array(&$topics, $type)
```

Type|Parameter|Description
---|---|---
`array`|`&$topics, $type`|desc

### integrate_ssi_queryMembers

```php
call_integration_hook('integrate_ssi_queryMembers', array(&$members)
```

Type|Parameter|Description
---|---|---
`array`|`&$members`|desc

### integrate_ssi_boardStats

```php
call_integration_hook('integrate_ssi_boardStats', array(&$totals)
```

Type|Parameter|Description
---|---|---
`array`|`&$totals`|desc

### integrate_ssi_whosOnline

```php
call_integration_hook('integrate_ssi_whosOnline', array(&$return)
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

### integrate_ssi_recentPoll

```php
call_integration_hook('integrate_ssi_recentPoll', array(&$return, $topPollInstead)
```

Type|Parameter|Description
---|---|---
`array`|`&$return, $topPollInstead`|desc

### integrate_ssi_showPoll

```php
call_integration_hook('integrate_ssi_showPoll', array(&$return)
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

### integrate_ssi_news

```php
call_integration_hook('integrate_ssi_news')
```

Type|Parameter|Description
---|---|---
`array`|``|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```

Type|Parameter|Description
---|---|---
`array`|`&$return, $eventOptions`|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```

Type|Parameter|Description
---|---|---
`array`|`&$return, $eventOptions`|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```

Type|Parameter|Description
---|---|---
`array`|`&$return, $eventOptions`|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```

Type|Parameter|Description
---|---|---
`array`|`&$return, $eventOptions`|desc

### integrate_ssi_boardNews

```php
call_integration_hook('integrate_ssi_boardNews', array(&$return)
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

### integrate_ssi_recentEvents

```php
call_integration_hook('integrate_ssi_recentEvents', array(&$return)
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc

### integrate_ssi_recentAttachments

```php
call_integration_hook('integrate_ssi_recentAttachments', array(&$attachments)
```

Type|Parameter|Description
---|---|---
`array`|`&$attachments`|desc
