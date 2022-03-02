---
layout: default
group: hooks
title: Membergroups
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_delete_membergroups

```php
call_integration_hook('integrate_delete_membergroups', array($groups))
```

Type|Parameter|Description
---|---|---
`array`|`$groups`|desc

Called from
: [`deleteMembergroups()` in `./Sources/Subs-Membergroups.php`](../docs/subs-membergroups.html#deletemembergroups)

Notes
: Since 2.1

### integrate_add_members_to_group

```php
call_integration_hook('integrate_add_members_to_group', array($members, $group, &$group_names))
```

Type|Parameter|Description
---|---|---
`array`|`$members`|desc
`array`|`$group`|desc
`array`|`&$group_names`|desc

Called from
: [`addMembersToGroup()` in `./Sources/Subs-Membergroups.php`](../docs/subs-membergroups.html#addmemberstogroup)

Notes
: Since 2.1

### integrate_getMembergroupList

```php
call_integration_hook('integrate_getMembergroupList', array(&$groupCache, $group))
```

Type|Parameter|Description
---|---|---
`array`|`&$groupCache`|desc
`array`|`$group`|desc

Called from
: [`cache_getMembergroupList()` in `./Sources/Subs-Membergroups.php`](../docs/subs-membergroups.html#cache_getmembergrouplist)

Notes
: Since 2.1

