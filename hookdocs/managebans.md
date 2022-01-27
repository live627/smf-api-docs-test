---
layout: default
group: hooks
title: ManageBans.php
count: 9
---
* auto-gen TOC:
{:toc}
### integrate_manage_bans

```php
call_integration_hook('integrate_manage_bans', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`Ban()` in `./Sources/ManageBans.php`](../docs/managebans.html#ban)

Notes
: Since 2.1

### integrate_ban_edit_list

```php
call_integration_hook('integrate_ban_edit_list', array(&$listOptions))
```

Type|Parameter|Description
---|---|---
`array`|`$&listOptions`|desc

Called from
: [`BanEdit()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit)

Notes
: Since 2.1

### integrate_ban_edit_new

```php
call_integration_hook('integrate_ban_edit_new', array())
```

Type|Parameter|Description
---|---|---

Called from
: [`BanEdit()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit)

Notes
: Since 2.1

### integrate_ban_list

```php
call_integration_hook('integrate_ban_list', array(&$ban_items))
```

Type|Parameter|Description
---|---|---
`array`|`$&ban_items`|desc

Called from
: [`list_getBanItems()` in `./Sources/ManageBans.php`](../docs/managebans.html#list_getbanitems)

Notes
: Since 2.1

### integrate_load_addtional_ip_ban

```php
call_integration_hook('integrate_load_addtional_ip_ban', array(&$search_list))
```

Type|Parameter|Description
---|---|---
`array`|`$&search_list`|desc

Called from
: [`banLoadAdditionalIPs()` in `./Sources/ManageBans.php`](../docs/managebans.html#banloadadditionalips)

Notes
: Since 2.1

### integrate_edit_bans

```php
call_integration_hook('integrate_edit_bans', array(&$ban_info, empty($_REQUEST['bg'])))
```

Type|Parameter|Description
---|---|---
`array`|`$&ban_info`|desc
`array`|`???`|desc

Called from
: [`banEdit2()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit2)

Notes
: Since 2.1

### integrate_edit_bans_post

```php
call_integration_hook('integrate_edit_bans_post', array())
```

Type|Parameter|Description
---|---|---

Called from
: [`banEdit2()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit2)

Notes
: Since 2.1

### integrate_save_triggers

```php
call_integration_hook('integrate_save_triggers', array(&$ban_triggers, &$ban_group))
```

Type|Parameter|Description
---|---|---
`array`|`$&ban_triggers`|desc
`array`|`$&ban_group`|desc

Called from
: [`saveTriggers()` in `./Sources/ManageBans.php`](../docs/managebans.html#savetriggers)

Notes
: Since 2.1

### integrate_remove_triggers

```php
call_integration_hook('integrate_remove_triggers', array(&$items_ids, $group_id))
```

Type|Parameter|Description
---|---|---
`array`|`$&items_ids`|desc
`array`|`$group_id`|desc

Called from
: [`removeBanTriggers()` in `./Sources/ManageBans.php`](../docs/managebans.html#removebantriggers)

Notes
: Since 2.1

