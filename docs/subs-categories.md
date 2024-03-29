---
layout: default
group: func
navtitle: Subs-Categories.php
title: ./Sources/Subs-Categories.php
count: 5
---
* auto-gen TOC:
{:toc}
### modifyCategory

```php
function modifyCategory(int $category_id, array $catOptions): void
```
Edit the position and properties of a category.

general function to modify the settings and position of a category.
used by ManageBoards.php to change the settings of a category.

Type|Parameter|Description
---|---|---
`int`|`$category_id`|The ID of the category
`array`|`$catOptions`|An array containing data and options related to the category

Integration hooks
: integrate_pre_modify_category
: integrate_modify_category

### createCategory

```php
function createCategory(array $catOptions): mixed
```
Create a new category.

general function to create a new category and set its position.
allows (almost) the same options as the modifyCat() function.
returns the ID of the newly created category.

Type|Parameter|Description
---|---|---
`array`|`$catOptions`|An array of data and settings related to the new category. Should have at least 'cat_name' and can also have 'cat_desc', 'move_after' and 'is_collapsable'

Integration hooks
: integrate_create_category

### deleteCategories

```php
function deleteCategories(array $categories, int $moveBoardsTo = null): void
```
Remove one or more categories.

general function to delete one or more categories.
allows to move all boards in the categories to a different category before deleting them.
if moveChildrenTo is set to null, all boards inside the given categories will be deleted.
deletes all information that's associated with the given categories.
updates the statistics to reflect the new situation.

Type|Parameter|Description
---|---|---
`array`|`$categories`|The IDs of the categories to delete
`int`|`$moveBoardsTo`|The ID of the category to move any boards to or null to delete the boards

Integration hooks
: integrate_delete_category

### setCategoryParsedDescription

```php
function setCategoryParsedDescription($category_info = array())
```
### getCategoriesParsedDescription

```php
function getCategoriesParsedDescription()
```
