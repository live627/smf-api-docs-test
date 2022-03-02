---
layout: default
group: hooks
title: Removetopic
count: 4
---
* auto-gen TOC:
{:toc}

## RemoveTopic.php
### integrate_remove_topics_before

```php
call_integration_hook('integrate_remove_topics_before', array($topics, $recycle_board))
```

Type|Parameter|Description
---|---|---
`array`|`$topics`|desc
`array`|`$recycle_board`|desc

Called from
: [`removeTopics()` in `./Sources/RemoveTopic.php`](../docs/removetopic.html#removetopics)

Notes
: Since 2.1

### integrate_remove_topics

```php
call_integration_hook('integrate_remove_topics', array($topics))
```

Type|Parameter|Description
---|---|---
`array`|`$topics`|desc

Called from
: [`removeTopics()` in `./Sources/RemoveTopic.php`](../docs/removetopic.html#removetopics)

Notes
: Since 2.1

### integrate_pre_remove_message

```php
call_integration_hook('integrate_pre_remove_message', array($message, $decreasePostCount, $row))
```

Type|Parameter|Description
---|---|---
`array`|`$message`|desc
`array`|`$decreasePostCount`|desc
`array`|`$row`|desc

Called from
: [`removeMessage()` in `./Sources/RemoveTopic.php`](../docs/removetopic.html#removemessage)

Notes
: Since 2.1

### integrate_remove_message

```php
call_integration_hook('integrate_remove_message', array($message, $row, $recycle))
```

Type|Parameter|Description
---|---|---
`array`|`$message`|desc
`array`|`$row`|desc
`array`|`$recycle`|desc

Called from
: [`removeMessage()` in `./Sources/RemoveTopic.php`](../docs/removetopic.html#removemessage)

Notes
: Since 2.1

