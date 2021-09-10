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
function showAttachment()
```
Downloads an avatar or attachment based on $_GET['attach'], and increments the download count.

It requires the view_attachments permission.
It disables the session parser, and clears any previous output.
It depends on the attachmentUploadDir setting being correct.
It is accessed via the query string ?action=dlattach.
Views to attachments do not increase hits and are not logged in the "Who's Online" log.

