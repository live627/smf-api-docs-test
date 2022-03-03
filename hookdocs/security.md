---
layout: default
group: hooks
title: Security
count: 9
---
* auto-gen TOC:
{:toc}
## Security.php
### integrate_validateSession

```php
call_integration_hook('integrate_validateSession', array(&$types))
```

Type|Parameter|Description
---|---|---
`array`|`&$types`|desc

Called from
: [`validateSession()` in `./Sources/Security.php`](../docs/security.html#validatesession)

Notes
: Since 2.1

### integrate_verify_password

```php
call_integration_hook('integrate_verify_password', array($user_info['username'], $_POST[$type . '_pass'], false))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc
`array`|`$_POST[$type . '_pass']`|desc
`array`|`false`|desc

Called from
: [`validateSession()` in `./Sources/Security.php`](../docs/security.html#validatesession)

Notes
: Since 1.1

### integrate_post_ban_permissions

```php
call_integration_hook('integrate_post_ban_permissions', array(&$denied_permissions))
```

Type|Parameter|Description
---|---|---
`array`|`&$denied_permissions`|desc

Called from
: [`banPermissions()` in `./Sources/Security.php`](../docs/security.html#banpermissions)

Notes
: Since 2.1

### integrate_warn_permissions

```php
call_integration_hook('integrate_warn_permissions', array(&$permission_change))
```

Type|Parameter|Description
---|---|---
`array`|`&$permission_change`|desc

Called from
: [`banPermissions()` in `./Sources/Security.php`](../docs/security.html#banpermissions)

Notes
: Since 2.1

### integrate_allowed_to_general

```php
call_integration_hook('integrate_allowed_to_general', array(&$user_permissions, $permission))
```

Type|Parameter|Description
---|---|---
`array`|`&$user_permissions`|desc
`array`|`$permission`|desc

Called from
: [`allowedTo()` in `./Sources/Security.php`](../docs/security.html#allowedto)

Notes
: Since 2.1

### integrate_allowed_to_board

```php
call_integration_hook('integrate_allowed_to_board', array(&$return, $permission, $boards, $any))
```

Type|Parameter|Description
---|---|---
`array`|`&$return`|desc
`array`|`$permission`|desc
`array`|`$boards`|desc
`array`|`$any`|desc

Called from
: [`allowedTo()` in `./Sources/Security.php`](../docs/security.html#allowedto)

Notes
: Since 2.1

### integrate_heavy_permissions_session

```php
call_integration_hook('integrate_heavy_permissions_session', array(&$heavy_permissions))
```

Type|Parameter|Description
---|---|---
`array`|`&$heavy_permissions`|desc

Called from
: [`isAllowedTo()` in `./Sources/Security.php`](../docs/security.html#isallowedto)

Notes
: Since 2.1

### integrate_boards_allowed_to

```php
call_integration_hook('integrate_boards_allowed_to', array(&$boards, $deny_boards, $permissions, $check_access, $simple))
```

Type|Parameter|Description
---|---|---
`array`|`&$boards`|desc
`array`|`$deny_boards`|desc
`array`|`$permissions`|desc
`array`|`$check_access`|desc
`array`|`$simple`|desc

Called from
: [`boardsAllowedTo()` in `./Sources/Security.php`](../docs/security.html#boardsallowedto)

Notes
: Since 2.1

### integrate_spam_protection

```php
call_integration_hook('integrate_spam_protection', array(&$timeOverrides))
```

Type|Parameter|Description
---|---|---
`array`|`&$timeOverrides`|desc

Called from
: [`spamProtection()` in `./Sources/Security.php`](../docs/security.html#spamprotection)

Notes
: Since 2.1

