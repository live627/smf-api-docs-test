---
layout: default
group: hooks
title: Likes
count: 4
---
* auto-gen TOC:
{:toc}
## Likes.php
### integrate_valid_likes

```php
call_integration_hook('integrate_valid_likes', array($this->_type, $this->_content, $this->_sa, $this->_js, $this->_extra))
```

Type|Parameter|Description
---|---|---
`array`|`$this->_type`|desc
`array`|`$this->_content`|desc
`array`|`$this->_sa`|desc
`array`|`$this->_js`|desc
`array`|`$this->_extra`|desc

Called from
: [`Likes::check()` in `./Sources/Likes.php`](../docs/likes.html#likes::check)

Notes
: Since 2.1

### integrate_issue_like_before

```php
call_integration_hook('integrate_issue_like_before', array(&$type, &$content, &$user, &$time))
```

Type|Parameter|Description
---|---|---
`array`|`&$type`|desc
`array`|`&$content`|desc
`array`|`&$user`|desc
`array`|`&$time`|desc

Called from
: [`Likes::insert()` in `./Sources/Likes.php`](../docs/likes.html#likes::insert)

Notes
: Since 2.1

### integrate_issue_like

```php
call_integration_hook('integrate_issue_like', array($this))
```

Type|Parameter|Description
---|---|---
`array`|`$this`|desc

Called from
: [`Likes::like()` in `./Sources/Likes.php`](../docs/likes.html#likes::like)

Notes
: Since 2.1

### integrate_likes_json_response

```php
call_integration_hook('integrate_likes_json_response', array(&$print))
```

Type|Parameter|Description
---|---|---
`array`|`&$print`|desc

Called from
: [`Likes::jsonResponse()` in `./Sources/Likes.php`](../docs/likes.html#likes::jsonresponse)

Notes
: Since 2.1

