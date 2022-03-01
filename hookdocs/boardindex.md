---
layout: default
group: hooks
title: BoardIndex.php
count: 1
---
* auto-gen TOC:
{:toc}

## BoardIndex.php
### integrate_mark_read_button

```php
call_integration_hook('integrate_mark_read_button')
```


Called from
: [`BoardIndex()` in `./Sources/BoardIndex.php`](../docs/boardindex.html#boardindex)

Notes
: Since 2.1


## Subs-BoardIndex.php
### integrate_pre_boardindex

```php
call_integration_hook('integrate_pre_boardindex', array(&$board_index_selects, &$board_index_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$board_index_selects`|desc
`array`|`&$board_index_parameters`|desc

Called from
: [`getBoardIndex()` in `./Sources/Subs-BoardIndex.php`](../docs/subs-boardindex.html#getboardindex)

Notes
: Since 2.1

### integrate_boardindex_board

```php
call_integration_hook('integrate_boardindex_board', array(&$this_category, $row_board))
```

Type|Parameter|Description
---|---|---
`array`|`&$this_category`|desc
`array`|`$row_board`|desc

Called from
: [`getBoardIndex()` in `./Sources/Subs-BoardIndex.php`](../docs/subs-boardindex.html#getboardindex)

Notes
: Since 2.1

### integrate_getboardtree

```php
call_integration_hook('integrate_getboardtree', array($board_index_options, &$this_category))
```

Type|Parameter|Description
---|---|---
`array`|`$board_index_options`|desc
`array`|`&$this_category`|desc

Called from
: [`getBoardIndex()` in `./Sources/Subs-BoardIndex.php`](../docs/subs-boardindex.html#getboardindex)

Notes
: Since 2.1

