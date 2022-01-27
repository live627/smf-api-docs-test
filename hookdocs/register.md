---
layout: default
group: hooks
title: Register.php
count: 2
---
* auto-gen TOC:
{:toc}
### integrate_activate

```php
call_integration_hook('integrate_activate', array($regOptions['username']))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc

Called from
: [`Register2()` in `./Sources/Register.php`](../docs/register.html#register2)

Notes
: Since 2.1

### integrate_activate

```php
call_integration_hook('integrate_activate', array($row['member_name']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc

Called from
: [`Activate()` in `./Sources/Register.php`](../docs/register.html#activate)

Notes
: Since 2.1

