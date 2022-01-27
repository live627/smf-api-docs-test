---
layout: default
group: hooks
title: ManageMembers.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_members

```php
call_integration_hook('integrate_manage_members', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ViewMembers()` in `./Sources/ManageMembers.php`](../docs/managemembers.html#viewmembers)

Notes
: Since 2.1

### integrate_view_members_params

```php
call_integration_hook('integrate_view_members_params', array(&$params))
```

Type|Parameter|Description
---|---|---
`array`|`$&params`|desc

Called from
: [`ViewMemberlist()` in `./Sources/ManageMembers.php`](../docs/managemembers.html#viewmemberlist)

Notes
: Since 2.1

### integrate_activate

```php
call_integration_hook('integrate_activate', array($member['username']))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc

Called from
: [`AdminApprove()` in `./Sources/ManageMembers.php`](../docs/managemembers.html#adminapprove)

Notes
: Since 2.1

