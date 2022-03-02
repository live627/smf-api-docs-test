---
layout: default
group: hooks
title: Categories
count: 4
---
* auto-gen TOC:
{:toc}
### integrate_pre_modify_category

```php
call_integration_hook('integrate_pre_modify_category', array($cat_id, &$catOptions))
```

Type|Parameter|Description
---|---|---
`array`|`$cat_id`|desc
`array`|`&$catOptions`|desc

Called from
: [`modifyCategory()` in `./Sources/Subs-Categories.php`](../docs/subs-categories.html#modifycategory)

Notes
: Since 2.1

### integrate_modify_category

```php
call_integration_hook('integrate_modify_category', array($cat_id, &$catUpdates, &$catParameters))
```

Type|Parameter|Description
---|---|---
`array`|`$cat_id`|desc
`array`|`&$catUpdates`|desc
`array`|`&$catParameters`|desc

Called from
: [`modifyCategory()` in `./Sources/Subs-Categories.php`](../docs/subs-categories.html#modifycategory)

Notes
: Since 2.1

### integrate_create_category

```php
call_integration_hook('integrate_create_category', array(&$catOptions, &$cat_columns, &$cat_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$catOptions`|desc
`array`|`&$cat_columns`|desc
`array`|`&$cat_parameters`|desc

Called from
: [`createCategory()` in `./Sources/Subs-Categories.php`](../docs/subs-categories.html#createcategory)

Notes
: Since 2.1

### integrate_delete_category

```php
call_integration_hook('integrate_delete_category', array($categories, &$moveBoardsTo))
```

Type|Parameter|Description
---|---|---
`array`|`$categories`|desc
`array`|`&$moveBoardsTo`|desc

Called from
: [`deleteCategories()` in `./Sources/Subs-Categories.php`](../docs/subs-categories.html#deletecategories)

Notes
: Since 2.1

