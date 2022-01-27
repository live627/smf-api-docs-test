---
layout: default
group: hooks
title: ManageBoards.php
count: 6
---
* auto-gen TOC:
{:toc}
### integrate_manage_boards

```php
call_integration_hook('integrate_manage_boards', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageBoards()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#manageboards)

Notes
: Since 2.1

### integrate_boards_main

```php
call_integration_hook('integrate_boards_main')
```


Called from
: [`ManageBoardsMain()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#manageboardsmain)

Notes
: Since 2.1

### integrate_edit_category

```php
call_integration_hook('integrate_edit_category')
```


Called from
: [`EditCategory()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editcategory)

Notes
: Since 2.1

### integrate_edit_board

```php
call_integration_hook('integrate_edit_board')
```


Called from
: [`EditBoard()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editboard)

Notes
: Since 2.1

### integrate_modify_board_settings

```php
call_integration_hook('integrate_modify_board_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`EditBoardSettings()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editboardsettings)

Notes
: Since 2.1

### integrate_save_board_settings

```php
call_integration_hook('integrate_save_board_settings')
```


Called from
: [`EditBoardSettings()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editboardsettings)

Notes
: Since 2.1

