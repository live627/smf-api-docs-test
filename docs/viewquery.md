---
layout: default
group: func
navtitle: ViewQuery.php
title: ./Sources/ViewQuery.php
count: 1
---
* auto-gen TOC:
{:toc}
### ViewQuery

```php
function ViewQuery()
```
Show the database queries for debugging
What this does:
- Toggles the session variable 'view_queries'.

- Views a list of queries and analyzes them.
- Requires the admin_forum permission.
- Is accessed via ?action=viewquery.
- Strings in this function have not been internationalized.

