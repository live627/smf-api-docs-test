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
: ssi_queryPosts()

### integrate_ssi_recentTopics

```php
call_integration_hook('integrate_ssi_recentTopics', array(&$posts)
```

Type|Parameter|Description
---|---|---
`array`|`&$posts`|List of posts

Called from
: ssi_recentTopics()

### integrate_ssi_topPoster

```php
call_integration_hook('integrate_ssi_topPoster', array(&$return)
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|List of members.

Called from
: ssi_topPoster()

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
`array`|`&$boards`|List of boards.

Called from
: ssi_topBoards()

Notes
: Each element has the following definition:

    Type|Key|Description
    ---|---|---
    `string`|`id`|The board id
    `string`|`num_posts`|Number of posts
    `string`|`num_topics`|Number of topcs
    `string`|`name`|The board real name; this is the name that can be changed at will
    `bool`|`new`|Whether it has new posts or not (in reverse)
    `string`|`href`|URL
    `string`|`link`|HTML formatted link to their profile
: Numeric values are strings because the native mysqld driver only returns strings.

### integrate_ssi_topTopics

```php
call_integration_hook('integrate_ssi_topTopics', array(&$topics, $type)
```

Type|Parameter|Description
---|---|---
`array`|`&$topics`|List of topics
`array`|`$type`|How the query was sorted; can be either `replies` or `views`

Called from
: ssi_toptopics()

Notes
: Each element has the following definition:

    Type|Key|Description
    ---|---|---
    `string`|`id`|The topic id
    `string`|`num_replies`|Number of replies
    `string`|`num_views`|Number of views
    `string`|`subject`|The subject of the topic
    `string`|`href`|URL
    `string`|`link`|HTML formatted link
: Numeric values are strings because the native mysqld driver only returns strings.

### integrate_ssi_queryMembers

```php
call_integration_hook('integrate_ssi_queryMembers', array(&$members)
```

Type|Parameter|Description
---|---|---
`array`|`&$members`|list of member ids

What...
: Srsly, why is this even here? This is the point wheere I wonder... what is the point of most of these SSI hooks?

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
