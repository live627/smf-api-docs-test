---
layout: default
group: hooks
title: Subs-Post.php
count: 12
---
* auto-gen TOC:
{:toc}
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

