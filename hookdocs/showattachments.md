---
layout: default
group: hooks
title: Showattachments
count: 2
---
* auto-gen TOC:
{:toc}

## ShowAttachments.php
### integrate_pre_download_request

```php
call_integration_hook('integrate_pre_download_request')
```


Called from
: [`showAttachment()` in `./Sources/ShowAttachments.php`](../docs/showattachments.html#showattachment)

Notes
: Since 2.1

### integrate_download_request

```php
call_integration_hook('integrate_download_request', array(&$attachRequest))
```

Type|Parameter|Description
---|---|---
`array`|`&$attachRequest`|desc

Called from
: [`showAttachment()` in `./Sources/ShowAttachments.php`](../docs/showattachments.html#showattachment)

Notes
: Since 2.1

