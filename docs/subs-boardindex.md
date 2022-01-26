---
layout: default
group: func
navtitle: Subs-BoardIndex.php
title: ./Sources/Subs-BoardIndex.php
count: 1
---
* auto-gen TOC:
{:toc}
### getBoardIndex

```php
function getBoardIndex(array $board_index_options): array
```
Fetches a list of boards and (optional) categories including
statistical information, child boards and moderators.

- Used by both the board index (main data) and the message index (child
boards).
	- Depending on the include_categories setting returns an associative
array with categories->boards->child_boards or an associative array
with boards->child_boards.

Type|Parameter|Description
---|---|---
`array`|`$board_index_options`|An array of boardindex options

