---
layout: default
group: hooks
title: Subs-Boards.php
count: 6
---
* auto-gen TOC:
{:toc}
### integrate_pre_modify_board

```php
call_integration_hook('integrate_pre_modify_board', array($id, &$boardOptions))
```

Type|Parameter|Description
---|---|---
`array`|`$id`|desc
`array`|`$&boardOptions`|desc

Called from
: [`modifyBoard()` in `./Sources/Subs-Boards.php`](../docs/subs-boards.html#modifyboard)

Notes
: Since 2.1

### integrate_modify_board

```php
call_integration_hook('integrate_modify_board', array($id, $boardOptions, &$boardUpdates, &$boardUpdateParameters))
```

Type|Parameter|Description
---|---|---
`array`|`$id`|desc
`array`|`$boardOptions`|desc
`array`|`$&boardUpdates`|desc
`array`|`$&boardUpdateParameters`|desc

Called from
: [`modifyBoard()` in `./Sources/Subs-Boards.php`](../docs/subs-boards.html#modifyboard)

Notes
: Since 2.1

### integrate_create_board

```php
call_integration_hook('integrate_create_board', array(&$boardOptions, &$board_columns, &$board_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`$&boardOptions`|desc
`array`|`$&board_columns`|desc
`array`|`$&board_parameters`|desc

Called from
: [`createBoard()` in `./Sources/Subs-Boards.php`](../docs/subs-boards.html#createboard)

Notes
: Since 2.1

### integrate_delete_board

```php
call_integration_hook('integrate_delete_board', array($boards_to_remove, &$moveChildrenTo))
```

Type|Parameter|Description
---|---|---
`array`|`$boards_to_remove`|desc
`array`|`$&moveChildrenTo`|desc

Called from
: [`deleteBoards()` in `./Sources/Subs-Boards.php`](../docs/subs-boards.html#deleteboards)

Notes
: Since 2.1

### integrate_pre_boardtree

```php
call_integration_hook('integrate_pre_boardtree', array(&$boardColumns, &$boardParameters, &$boardJoins, &$boardWhere, &$boardOrder))
```

Type|Parameter|Description
---|---|---
`array`|`$&boardColumns`|desc
`array`|`$&boardParameters`|desc
`array`|`$&boardJoins`|desc
`array`|`$&boardWhere`|desc
`array`|`$&boardOrder`|desc

Called from
: [`getBoardTree()` in `./Sources/Subs-Boards.php`](../docs/subs-boards.html#getboardtree)

Notes
: Since 2.1

### integrate_boardtree_board

```php
call_integration_hook('integrate_boardtree_board', array($row))
```

Type|Parameter|Description
---|---|---
`array`|`$row`|desc

Called from
: [`getBoardTree()` in `./Sources/Subs-Boards.php`](../docs/subs-boards.html#getboardtree)

Notes
: Since 2.1

