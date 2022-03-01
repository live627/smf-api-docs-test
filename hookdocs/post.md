---
layout: default
group: hooks
title: Post.php
count: 11
---
* auto-gen TOC:
{:toc}

## Post.php
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


## Subs-Post.php
### integrate_preparsecode

```php
call_integration_hook('integrate_preparsecode', array(&$message, $previewing))
```

Type|Parameter|Description
---|---|---
`array`|`&$message`|desc
`array`|`$previewing`|desc

Called from
: [`preparsecode()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#preparsecode)

Notes
: Since 2.1

### integrate_unpreparsecode

```php
call_integration_hook('integrate_unpreparsecode', array(&$message))
```

Type|Parameter|Description
---|---|---
`array`|`&$message`|desc

Called from
: [`un_preparsecode()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#un_preparsecode)

Notes
: Since 2.1

### integrate_outgoing_email

```php
call_integration_hook('integrate_outgoing_email', array(&$subject, &$message, &$headers, &$to_array))
```

Type|Parameter|Description
---|---|---
`array`|`&$subject`|desc
`array`|`&$message`|desc
`array`|`&$headers`|desc
`array`|`&$to_array`|desc

Called from
: [`sendmail()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#sendmail)

Notes
: Since 2.1

### integrate_personal_message

```php
call_integration_hook('integrate_personal_message', array(&$recipients, &$from, &$subject, &$message))
```

Type|Parameter|Description
---|---|---
`array`|`&$recipients`|desc
`array`|`&$from`|desc
`array`|`&$subject`|desc
`array`|`&$message`|desc

Called from
: [`sendpm()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#sendpm)

Notes
: Since 2.1

### integrate_personal_message_after

```php
call_integration_hook('integrate_personal_message_after', array(&$id_pm, &$log, &$recipients, &$from, &$subject, &$message))
```

Type|Parameter|Description
---|---|---
`array`|`&$id_pm`|desc
`array`|`&$log`|desc
`array`|`&$recipients`|desc
`array`|`&$from`|desc
`array`|`&$subject`|desc
`array`|`&$message`|desc

Called from
: [`sendpm()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#sendpm)

Notes
: Since 2.1

### integrate_create_post

```php
call_integration_hook('integrate_create_post', array(&$msgOptions, &$topicOptions, &$posterOptions, &$message_columns, &$message_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$msgOptions`|desc
`array`|`&$topicOptions`|desc
`array`|`&$posterOptions`|desc
`array`|`&$message_columns`|desc
`array`|`&$message_parameters`|desc

Called from
: [`createPost()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#createpost)

Notes
: Since 2.1

### integrate_after_create_post

```php
call_integration_hook('integrate_after_create_post', array($msgOptions, $topicOptions, $posterOptions, $message_columns, $message_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`$msgOptions`|desc
`array`|`$topicOptions`|desc
`array`|`$posterOptions`|desc
`array`|`$message_columns`|desc
`array`|`$message_parameters`|desc

Called from
: [`createPost()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#createpost)

Notes
: Since 2.1

### integrate_before_create_topic

```php
call_integration_hook('integrate_before_create_topic', array(&$msgOptions, &$topicOptions, &$posterOptions, &$topic_columns, &$topic_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$msgOptions`|desc
`array`|`&$topicOptions`|desc
`array`|`&$posterOptions`|desc
`array`|`&$topic_columns`|desc
`array`|`&$topic_parameters`|desc

Called from
: [`createPost()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#createpost)

Notes
: Since 2.1

### integrate_create_topic

```php
call_integration_hook('integrate_create_topic', array(&$msgOptions, &$topicOptions, &$posterOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$msgOptions`|desc
`array`|`&$topicOptions`|desc
`array`|`&$posterOptions`|desc

Called from
: [`createPost()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#createpost)

Notes
: Since 2.1

### integrate_modify_topic

```php
call_integration_hook('integrate_modify_topic', array(&$topics_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$topics_columns`|desc
`array`|`&$update_parameters`|desc
`array`|`&$msgOptions`|desc
`array`|`&$topicOptions`|desc
`array`|`&$posterOptions`|desc

Called from
: [`createPost()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#createpost)

Notes
: Since 2.1

### integrate_modify_post

```php
call_integration_hook('integrate_modify_post', array(&$messages_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions, &$messageInts))
```

Type|Parameter|Description
---|---|---
`array`|`&$messages_columns`|desc
`array`|`&$update_parameters`|desc
`array`|`&$msgOptions`|desc
`array`|`&$topicOptions`|desc
`array`|`&$posterOptions`|desc
`array`|`&$messageInts`|desc

Called from
: [`modifyPost()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#modifypost)

Notes
: Since 2.1

### integrate_after_approve_posts

```php
call_integration_hook('integrate_after_approve_posts', array($approve, $msgs, $topic_changes, $member_post_changes))
```

Type|Parameter|Description
---|---|---
`array`|`$approve`|desc
`array`|`$msgs`|desc
`array`|`$topic_changes`|desc
`array`|`$member_post_changes`|desc

Called from
: [`approvePosts()` in `./Sources/Subs-Post.php`](../docs/subs-post.html#approveposts)

Notes
: Since 2.1

