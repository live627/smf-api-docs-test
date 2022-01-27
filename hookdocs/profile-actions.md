---
layout: default
group: hooks
title: Profile-Actions.php
count: 1
---
* auto-gen TOC:
{:toc}
### integrate_activate

```php
call_integration_hook('integrate_activate', array($user_profile[$memID]['member_name']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc

Called from
: [`activateAccount()` in `./Sources/Profile-Actions.php`](../docs/profile-actions.html#activateaccount)

Notes
: Since 2.1

