---
layout: default
group: func
navtitle: Subs-Boards.php
title: ./Sources/Subs-Boards.php
count: 18
---
* auto-gen TOC:
{:toc}
### markBoardsRead

```php
function markBoardsRead(int|array $boards, bool $unread = false): void
```
Mark a board or multiple boards read.



Type|Parameter|Description
---|---|---
`int`&#124;`array`|`$boards`|The ID of a single board or an array of boards
`bool`|`$unread`|Whether we're marking them as unread

### MarkRead

```php
function MarkRead(): void
```
Mark one or more boards as read.



### getMsgMemberID

```php
function getMsgMemberID(int $messageID): int
```
Get the id_member associated with the specified message.



Type|Parameter|Description
---|---|---
`int`|`$messageID`|The ID of the message

### modifyBoard

```php
function modifyBoard(int $board_id, array &$boardOptions): void
```
Modify the settings and position of a board.

Used by ManageBoards.php to change the settings of a board.

Type|Parameter|Description
---|---|---
`int`|`$board_id`|The ID of the board
`array`|`\&$boardOptions`|An array of options related to the board

Integration hooks
: integrate_pre_modify_board
: integrate_modify_board

### createBoard

```php
function createBoard(array $boardOptions): int
```
Create a new board and set its properties and position.

Allows (almost) the same options as the modifyBoard() function.
With the option inherit_permissions set, the parent board permissions
will be inherited.

Type|Parameter|Description
---|---|---
`array`|`$boardOptions`|An array of information for the new board

Integration hooks
: integrate_create_board

### deleteBoards

```php
function deleteBoards(array $boards_to_remove, int $moveChildrenTo = null): void
```
Remove one or more boards.

Allows to move the children of the board before deleting it
if moveChildrenTo is set to null, the child boards will be deleted.
Deletes:
  - all topics that are on the given boards;
  - all information that's associated with the given boards;
updates the statistics to reflect the new situation.

Type|Parameter|Description
---|---|---
`array`|`$boards_to_remove`|The boards to remove
`int`|`$moveChildrenTo`|The ID of the board to move the child boards to (null to remove the child boards, 0 to make them a top-level board)

Integration hooks
: integrate_delete_board

### reorderBoards

```php
function reorderBoards(): void
```
Put all boards in the right order and sorts the records of the boards table.

Used by modifyBoard(), deleteBoards(), modifyCategory(), and deleteCategories() functions

### fixChildren

```php
function fixChildren(int $parent, int $newLevel, int $newParent): void
```
Fixes the children of a board by setting their child_levels to new values.

Used when a board is deleted or moved, to affect its children.

Type|Parameter|Description
---|---|---
`int`|`$parent`|The ID of the parent board
`int`|`$newLevel`|The new child level for each of the child boards
`int`|`$newParent`|The ID of the new parent board

### getTreeOrder

```php
function getTreeOrder(): array
```
Tries to load up the entire board order and category very very quickly
Returns an array with two elements, cats and boards



### sortBoards

```php
function sortBoards(array &$boards): void
```
Takes a board array and sorts it



Type|Parameter|Description
---|---|---
`array`|`\&$boards`|The boards

### sortCategories

```php
function sortCategories(array &$categories): void
```
Takes a category array and sorts it



Type|Parameter|Description
---|---|---
`array`|`\&$categories`|The categories

### getBoardModerators

```php
function getBoardModerators(array $boards): array
```
Returns the given board's moderators, with their names and links



Type|Parameter|Description
---|---|---
`array`|`$boards`|The boards to get moderators of

### getBoardModeratorGroups

```php
function getBoardModeratorGroups(array $boards): array
```
Returns board's moderator groups with their names and link



Type|Parameter|Description
---|---|---
`array`|`$boards`|The boards to get moderator groups of

### getBoardTree

```php
function getBoardTree(): void
```
Load a lot of useful information regarding the boards and categories.

The information retrieved is stored in globals:
$boards		properties of each board.
$boardList	a list of boards grouped by category ID.
$cat_tree	properties of each category.

Integration hooks
: integrate_pre_boardtree
: integrate_boardtree_board

### recursiveBoards

```php
function recursiveBoards(array &$_boardList, array &$_tree): void
```
Recursively get a list of boards.

Used by getBoardTree

Type|Parameter|Description
---|---|---
`array`|`\&$_boardList`|The board list
`array`|`\&$_tree`|The board tree

### isChildOf

```php
function isChildOf(int $child, int $parent): bool
```
Returns whether the child board id is actually a child of the parent (recursive).



Type|Parameter|Description
---|---|---
`int`|`$child`|The ID of the child board
`int`|`$parent`|The ID of a parent board

### setBoardParsedDescription

```php
function setBoardParsedDescription($category_id = 0, $boards_info = array())
```
### getBoardsParsedDescription

```php
function getBoardsParsedDescription($category_id = 0)
```
