---
layout: default
group: func
navtitle: ManageBoards.php
title: ./Sources/ManageBoards.php
count: 8
---
* auto-gen TOC:
{:toc}
### ManageBoards

```php
function ManageBoards(): void
```
The main dispatcher; doesn't do anything, just delegates.

This is the main entry point for all the manageboards admin screens.
Called by ?action=admin;area=manageboards.
It checks the permissions, based on the sub-action, and calls a function based on the sub-action.

Uses ManageBoards language file.

Integration hooks
: integrate_manage_boards

### ManageBoardsMain

```php
function ManageBoardsMain(): void
```
The main control panel thing, the screen showing all boards and categories.

Called by ?action=admin;area=manageboards or ?action=admin;area=manageboards;sa=move.
Requires manage_boards permission.
It also handles the interface for moving boards.

Uses ManageBoards template, main sub-template.

Integration hooks
: integrate_boards_main

### EditCategory

```php
function EditCategory(): void
```
Modify a specific category.

(screen for editing and repositioning a category.)
Also used to show the confirm deletion of category screen
(sub-template confirm_category_delete).
Called by ?action=admin;area=manageboards;sa=cat
Requires manage_boards permission.

Integration hooks
: integrate_edit_category

### EditCategory2

```php
function EditCategory2(): void
```
Function for handling a submitted form saving the category.

(complete the modifications to a specific category.)
It also handles deletion of a category.
It requires manage_boards permission.
Called by ?action=admin;area=manageboards;sa=cat2
Redirects to ?action=admin;area=manageboards.

### EditBoard

```php
function EditBoard(): void
```
Modify a specific board...
screen for editing and repositioning a board.

called by ?action=admin;area=manageboards;sa=board
uses the modify_board sub-template of the ManageBoards template.
requires manage_boards permission.
also used to show the confirm deletion of category screen (sub-template confirm_board_delete).

Integration hooks
: integrate_edit_board

### EditBoard2

```php
function EditBoard2(): void
```
Make changes to/delete a board.

(function for handling a submitted form saving the board.)
It also handles deletion of a board.
Called by ?action=admin;area=manageboards;sa=board2
Redirects to ?action=admin;area=manageboards.
It requires manage_boards permission.

### ModifyCat

```php
function ModifyCat(): void
```
Used to retrieve data for modifying a board category



### EditBoardSettings

```php
function EditBoardSettings(bool $return_config = false): void|array
```
A screen to set a few general board and category settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config_vars array (used for admin search)

Integration hooks
: integrate_modify_board_settings
: integrate_save_board_settings

