---
layout: default
group: hooks
title: Poll
count: 3
---
* auto-gen TOC:
{:toc}
## Poll.php
### integrate_poll_vote

```php
call_integration_hook('integrate_poll_vote', array(&$row['id_poll'], &$pollOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$id_poll`|desc
`array`|`&$pollOptions`|desc

Called from
: [`Vote()` in `./Sources/Poll.php`](../docs/poll.html#vote)

Notes
: Since 2.1

### integrate_poll_add_edit

```php
call_integration_hook('integrate_poll_add_edit', array($bcinfo['id_poll'], $isEdit))
```

Type|Parameter|Description
---|---|---
`array`|`$id_poll`|desc
`array`|`$isEdit`|desc

Called from
: [`EditPoll2()` in `./Sources/Poll.php`](../docs/poll.html#editpoll2)

Notes
: Since 2.1

### integrate_poll_remove

```php
call_integration_hook('integrate_poll_remove', array($pollID))
```

Type|Parameter|Description
---|---|---
`array`|`$pollID`|desc

Called from
: [`RemovePoll()` in `./Sources/Poll.php`](../docs/poll.html#removepoll)

Notes
: Since 2.1

