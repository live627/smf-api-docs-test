---
layout: default
group: hooks
title: Subs-Auth.php
count: 7
---
* auto-gen TOC:
{:toc}
### integrate_cookie_data

```php
call_integration_hook('integrate_cookie_data', array($data, &$custom_data))
```

Type|Parameter|Description
---|---|---
`array`|`$data`|desc
`array`|`&$custom_data`|desc

Called from
: [`setLoginCookie()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#setlogincookie)

Notes
: Since 2.1

### integrate_validateSession

```php
call_integration_hook('integrate_validateSession', array(&$types))
```

Type|Parameter|Description
---|---|---
`array`|`&$types`|desc

Called from
: [`adminLogin()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#adminlogin)

Notes
: Since 2.1

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($old_user, $user, $newPassword))
```

Type|Parameter|Description
---|---|---
`array`|`$old_user`|desc
`array`|`$user`|desc
`array`|`$newPassword`|desc

Called from
: [`resetPassword()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#resetpassword)

Notes
: Since 2.1

### integrate_validate_username

```php
call_integration_hook('integrate_validate_username', array($username, &$errors))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc
`array`|`&$errors`|desc

Called from
: [`validateUsername()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#validateusername)

Notes
: Since 2.1

### integrate_validatePassword

```php
call_integration_hook('integrate_validatePassword', array($password, $username, $restrict_in, &$pass_error))
```

Type|Parameter|Description
---|---|---
`array`|`$password`|desc
`array`|`$username`|desc
`array`|`$restrict_in`|desc
`array`|`&$pass_error`|desc

Called from
: [`validatePassword()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#validatepassword)

Notes
: Since 2.1

### integrate_mod_cache

```php
call_integration_hook('integrate_mod_cache')
```


Called from
: [`rebuildModCache()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#rebuildmodcache)

Notes
: Since 2.1

### integrate_cookie

```php
call_integration_hook('integrate_cookie', array($name, $value, $expire, $path, $domain, $secure, $httponly, $samesite))
```

Type|Parameter|Description
---|---|---
`array`|`$name`|desc
`array`|`$value`|desc
`array`|`$expire`|desc
`array`|`$path`|desc
`array`|`$domain`|desc
`array`|`$secure`|desc
`array`|`$httponly`|desc
`array`|`$samesite`|desc

Called from
: [`smf_setcookie()` in `./Sources/Subs-Auth.php`](../docs/subs-auth.html#smf_setcookie)

Notes
: Since 2.1

