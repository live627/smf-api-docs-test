---
layout: default
group: hooks
title: Reminder
count: 2
---
* auto-gen TOC:
{:toc}

## Reminder.php
### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($username, $username, $_POST['passwrd1']))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc
`array`|`$username`|desc
`array`|`$passwrd1`|desc

Called from
: [`setPassword2()` in `./Sources/Reminder.php`](../docs/reminder.html#setpassword2)

Notes
: Since 2.1

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($row['member_name'], $row['member_name'], $_POST['passwrd1']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc
`array`|`$member_name`|desc
`array`|`$passwrd1`|desc

Called from
: [`SecretAnswer2()` in `./Sources/Reminder.php`](../docs/reminder.html#secretanswer2)

Notes
: Since 2.1

