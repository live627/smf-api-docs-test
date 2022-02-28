---
layout: default
group: hooks
title: Post.php
count: 11
---
* auto-gen TOC:
{:toc}
### integrate_post_start

```php
call_integration_hook('integrate_post_start')
```


Called from
: [`Post()` in `./Sources/Post.php`](../docs/post.html#post)

Notes
: Since 2.1

### integrate_preview_post

```php
call_integration_hook('integrate_preview_post', array(&$form_message, &$form_subject))
```

Type|Parameter|Description
---|---|---
`array`|`&$form_message`|desc
`array`|`&$form_subject`|desc

Called from
: [`Post()` in `./Sources/Post.php`](../docs/post.html#post)

Notes
: Since 2.1

### integrate_post_errors

```php
call_integration_hook('integrate_post_errors', array(&$post_errors, &$minor_errors, $form_message, $form_subject))
```

Type|Parameter|Description
---|---|---
`array`|`&$post_errors`|desc
`array`|`&$minor_errors`|desc
`array`|`$form_message`|desc
`array`|`$form_subject`|desc

Called from
: [`Post()` in `./Sources/Post.php`](../docs/post.html#post)

Notes
: Since 2.1

### integrate_post_end

```php
call_integration_hook('integrate_post_end')
```


Called from
: [`Post()` in `./Sources/Post.php`](../docs/post.html#post)

Notes
: Since 2.1

### integrate_post2_start

```php
call_integration_hook('integrate_post2_start', array(&$post_errors))
```

Type|Parameter|Description
---|---|---
`array`|`&$post_errors`|desc

Called from
: [`Post2()` in `./Sources/Post.php`](../docs/post.html#post2)

Notes
: Since 2.1

### integrate_post2_pre

```php
call_integration_hook('integrate_post2_pre', array(&$post_errors))
```

Type|Parameter|Description
---|---|---
`array`|`&$post_errors`|desc

Called from
: [`Post2()` in `./Sources/Post.php`](../docs/post.html#post2)

Notes
: Since 2.1

### integrate_poll_add_edit

```php
call_integration_hook('integrate_poll_add_edit', array($id_poll, false))
```

Type|Parameter|Description
---|---|---
`array`|`$id_poll`|desc
`array`|`false`|desc

Called from
: [`Post2()` in `./Sources/Post.php`](../docs/post.html#post2)

Notes
: Since 2.1

### integrate_post2_end

```php
call_integration_hook('integrate_post2_end')
```


Called from
: [`Post2()` in `./Sources/Post.php`](../docs/post.html#post2)

Notes
: Since 2.1

### integrate_getTopic_previous_post

```php
call_integration_hook('integrate_getTopic_previous_post', array(&$row))
```

Type|Parameter|Description
---|---|---
`array`|`&$row`|desc

Called from
: [`getTopic()` in `./Sources/Post.php`](../docs/post.html#gettopic)

Notes
: Since 2.1

### integrate_post_JavascriptModify

```php
call_integration_hook('integrate_post_JavascriptModify', array(&$post_errors, $row))
```

Type|Parameter|Description
---|---|---
`array`|`&$post_errors`|desc
`array`|`$row`|desc

Called from
: [`JavaScriptModify()` in `./Sources/Post.php`](../docs/post.html#javascriptmodify)

Notes
: Since 2.1

### integrate_jsmodify_xml

```php
call_integration_hook('integrate_jsmodify_xml')
```


Called from
: [`JavaScriptModify()` in `./Sources/Post.php`](../docs/post.html#javascriptmodify)

Notes
: Since 2.1

