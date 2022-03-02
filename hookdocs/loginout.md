---
layout: default
group: hooks
title: Loginout
count: 4
---
* auto-gen TOC:
{:toc}

## LogInOut.php
### integrate_validate_login

```php
call_integration_hook('integrate_validate_login', array($_POST['user'], isset($_POST['passwrd']))
```

Type|Parameter|Description
---|---|---
`array`|`$user`|desc
`array`|`isset($passwrd`|desc

Called from
: [`Login2()` in `./Sources/LogInOut.php`](../docs/loginout.html#login2)

Notes
: Since 2.1

### integrate_other_passwords

```php
call_integration_hook('integrate_other_passwords', array(&$other_passwords))
```

Type|Parameter|Description
---|---|---
`array`|`&$other_passwords`|desc

Called from
: [`Login2()` in `./Sources/LogInOut.php`](../docs/loginout.html#login2)

Notes
: Since 2.1

### integrate_login

```php
call_integration_hook('integrate_login', array($user_settings['member_name'], null, $modSettings['cookieTime']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc
`array`|`null`|desc
`array`|`$cookieTime`|desc

Called from
: [`DoLogin()` in `./Sources/LogInOut.php`](../docs/loginout.html#dologin)

Notes
: Since 2.1

### integrate_logout

```php
call_integration_hook('integrate_logout', array($user_settings['member_name']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc

Called from
: [`Logout()` in `./Sources/LogInOut.php`](../docs/loginout.html#logout)

Notes
: Since 2.1

