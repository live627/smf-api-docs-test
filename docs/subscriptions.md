---
layout: default
group: func
navtitle: subscriptions.php
title: ./subscriptions.php
count: 1
---
* auto-gen TOC:
{:toc}
### generateSubscriptionError

```php
function generateSubscriptionError(string $text, bool $debug = false): void
```
Log an error then exit



Type|Parameter|Description
---|---|---
`string`|`$text`|The error to log
`bool`|`$debug`|If true, won't send an email if $modSettings['paid_email'] isn't set

