---
layout: default
group: func
navtitle: ShowAttachments.php
title: ./Sources/ShowAttachments.php
count: 1
---
* auto-gen TOC:
{:toc}
### showAttachment

```php
function showAttachment(): void
```
Downloads an avatar or attachment based on $_GET['attach'], and increments the download count.

It requires the view_attachments permission.
It disables the session parser, and clears any previous output.
It depends on the attachmentUploadDir setting being correct.
It is accessed via the query string ?action=dlattach.
Views to attachments do not increase hits and are not logged in the "Who's Online" log.

Integration hooks
: integrate_pre_download_request
: integrate_download_request

