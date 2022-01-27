---
layout: default
group: hooks
title: ManagePaid.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_subscriptions

```php
call_integration_hook('integrate_manage_subscriptions', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManagePaidSubscriptions()` in `./Sources/ManagePaid.php`](../docs/managepaid.html#managepaidsubscriptions)

Notes
: Since 2.1

### integrate_delete_subscription

```php
call_integration_hook('integrate_delete_subscription', array($context['sub_id']))
```

Type|Parameter|Description
---|---|---
`array`|`$sub_id`|desc

Called from
: [`ModifySubscription()` in `./Sources/ManagePaid.php`](../docs/managepaid.html#modifysubscription)

Notes
: Since 2.1

### integrate_save_subscription

```php
call_integration_hook('integrate_save_subscription', array($context['action_type'] == 'add' ? $id_subscribe : $context['sub_id'], $_POST['name'], $_POST['desc'], $isActive, $span, $cost, $_POST['prim_group'], $addgroups, $isRepeatable, $allowpartial, $emailComplete, $reminder))
```

Type|Parameter|Description
---|---|---
`array`|`???`|desc
`array`|`$name`|desc
`array`|`$desc`|desc
`array`|`$isActive`|desc
`array`|`$span`|desc
`array`|`$cost`|desc
`array`|`$prim_group`|desc
`array`|`$addgroups`|desc
`array`|`$isRepeatable`|desc
`array`|`$allowpartial`|desc
`array`|`$emailComplete`|desc
`array`|`$reminder`|desc

Called from
: [`ModifySubscription()` in `./Sources/ManagePaid.php`](../docs/managepaid.html#modifysubscription)

Notes
: Since 2.1

