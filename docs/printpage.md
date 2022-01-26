---
layout: default
group: func
navtitle: Printpage.php
title: ./Sources/Printpage.php
count: 1
---
* auto-gen TOC:
{:toc}
### PrintTopic

```php
function PrintTopic(): void
```
Format a topic to be printer friendly.

Must be called with a topic specified.
Accessed via ?action=printpage.

Uses Printpage template, main sub-template.
Uses print_above/print_below later without the main layer.

