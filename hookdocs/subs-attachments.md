---
layout: default
group: hooks
title: Subs-Attachments.php
count: 5
---
* auto-gen TOC:
{:toc}
### integrate_attachment_upload

```php
call_integration_hook('integrate_attachment_upload', array())
```

Type|Parameter|Description
---|---|---

Called from
: [`processAttachments()` in `./Sources/Subs-Attachments.php`](../docs/subs-attachments.html#processattachments)

Notes
: Since 2.1

### integrate_createAttachment

```php
call_integration_hook('integrate_createAttachment', array(&$attachmentOptions, &$attachmentInserts))
```

Type|Parameter|Description
---|---|---
`array`|`$&attachmentOptions`|desc
`array`|`$&attachmentInserts`|desc

Called from
: [`createAttachment()` in `./Sources/Subs-Attachments.php`](../docs/subs-attachments.html#createattachment)

Notes
: Since 2.1

### integrate_assign_attachments

```php
call_integration_hook('integrate_assign_attachments', array(&$attachIDs, &$msgID))
```

Type|Parameter|Description
---|---|---
`array`|`$&attachIDs`|desc
`array`|`$&msgID`|desc

Called from
: [`assignAttachments()` in `./Sources/Subs-Attachments.php`](../docs/subs-attachments.html#assignattachments)

Notes
: Since 2.1

### integrate_pre_parseAttachBBC

```php
call_integration_hook('integrate_pre_parseAttachBBC', array($attachID, $msgID))
```

Type|Parameter|Description
---|---|---
`array`|`$attachID`|desc
`array`|`$msgID`|desc

Called from
: [`parseAttachBBC()` in `./Sources/Subs-Attachments.php`](../docs/subs-attachments.html#parseattachbbc)

Notes
: Since 2.1

### integrate_post_parseAttachBBC

```php
call_integration_hook('integrate_post_parseAttachBBC', array(&$attachContext))
```

Type|Parameter|Description
---|---|---
`array`|`$&attachContext`|desc

Called from
: [`parseAttachBBC()` in `./Sources/Subs-Attachments.php`](../docs/subs-attachments.html#parseattachbbc)

Notes
: Since 2.1

