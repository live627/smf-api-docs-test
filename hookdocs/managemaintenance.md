---
layout: default
group: hooks
title: ManageMaintenance.php
count: 2
---
* auto-gen TOC:
{:toc}
### integrate_manage_maintenance

```php
call_integration_hook('integrate_manage_maintenance', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageMaintenance()` in `./Sources/ManageMaintenance.php`](../docs/managemaintenance.html#managemaintenance)

Notes
: Since 2.1

### integrate_convert_msgbody

```php
call_integration_hook('integrate_convert_msgbody', array($body_type))
```

Type|Parameter|Description
---|---|---
`array`|`$body_type`|desc

Called from
: [`ConvertMsgBody()` in `./Sources/ManageMaintenance.php`](../docs/managemaintenance.html#convertmsgbody)

Notes
: Since 2.1

