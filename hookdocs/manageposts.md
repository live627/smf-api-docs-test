---
layout: default
group: hooks
title: ManagePosts.php
count: 7
---
* auto-gen TOC:
{:toc}
### integrate_manage_posts

```php
call_integration_hook('integrate_manage_posts', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManagePostSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#managepostsettings)

Notes
: Since 2.1

### integrate_save_censors

```php
call_integration_hook('integrate_save_censors', array(&$updates))
```

Type|Parameter|Description
---|---|---
`array`|`$&updates`|desc

Called from
: [`SetCensor()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#setcensor)

Notes
: Since 2.1

### integrate_censors

```php
call_integration_hook('integrate_censors')
```


Called from
: [`SetCensor()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#setcensor)

Notes
: Since 2.1

### integrate_modify_post_settings

```php
call_integration_hook('integrate_modify_post_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyPostSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifypostsettings)

Notes
: Since 2.1

### integrate_save_post_settings

```php
call_integration_hook('integrate_save_post_settings')
```


Called from
: [`ModifyPostSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifypostsettings)

Notes
: Since 2.1

### integrate_modify_topic_settings

```php
call_integration_hook('integrate_modify_topic_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyTopicSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifytopicsettings)

Notes
: Since 2.1

### integrate_save_topic_settings

```php
call_integration_hook('integrate_save_topic_settings')
```


Called from
: [`ModifyTopicSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifytopicsettings)

Notes
: Since 2.1

