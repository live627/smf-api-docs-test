---
layout: default
group: hooks
title: Subs-Members.php
count: 8
---
* auto-gen TOC:
{:toc}
### integrate_delete_members

```php
call_integration_hook('integrate_delete_members', array($users))
```

Type|Parameter|Description
---|---|---
`array`|`$users`|desc

Called from
: [`deleteMembers()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#deletemembers)

Notes
: Since 2.1

### integrate_register_check

```php
call_integration_hook('integrate_register_check', array(&$regOptions, &$reg_errors))
```

Type|Parameter|Description
---|---|---
`array`|`$&regOptions`|desc
`array`|`$&reg_errors`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_register

```php
call_integration_hook('integrate_register', array(&$regOptions, &$theme_vars, &$knownInts, &$knownFloats))
```

Type|Parameter|Description
---|---|---
`array`|`$&regOptions`|desc
`array`|`$&theme_vars`|desc
`array`|`$&knownInts`|desc
`array`|`$&knownFloats`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_post_register

```php
call_integration_hook('integrate_post_register', array(&$regOptions, &$theme_vars, &$memberID))
```

Type|Parameter|Description
---|---|---
`array`|`$&regOptions`|desc
`array`|`$&theme_vars`|desc
`array`|`$&memberID`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_register_after

```php
call_integration_hook('integrate_register_after', array($regOptions, $memberID))
```

Type|Parameter|Description
---|---|---
`array`|`$regOptions`|desc
`array`|`$memberID`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_check_name

```php
call_integration_hook('integrate_check_name', array($checkName, &$is_reserved, $current_id_member, $is_name))
```

Type|Parameter|Description
---|---|---
`array`|`$checkName`|desc
`array`|`$&is_reserved`|desc
`array`|`$current_id_member`|desc
`array`|`$is_name`|desc

Called from
: [`isReservedName()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#isreservedname)

Notes
: Since 2.1

### integrate_groups_allowed_to

```php
call_integration_hook('integrate_groups_allowed_to', array(&$member_groups, $permission, $board_id))
```

Type|Parameter|Description
---|---|---
`array`|`$&member_groups`|desc
`array`|`$permission`|desc
`array`|`$board_id`|desc

Called from
: [`groupsAllowedTo()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#groupsallowedto)

Notes
: Since 2.1

### integrate_reattribute_posts

```php
call_integration_hook('integrate_reattribute_posts', array($memID, $email, $membername, $post_count, &$updated))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc
`array`|`$email`|desc
`array`|`$membername`|desc
`array`|`$post_count`|desc
`array`|`$&updated`|desc

Called from
: [`reattributePosts()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#reattributeposts)

Notes
: Since 2.1

