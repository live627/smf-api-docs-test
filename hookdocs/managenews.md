---
layout: default
group: hooks
title: ManageNews.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_manage_news

```php
call_integration_hook('integrate_manage_news', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageNews()` in `./Sources/ManageNews.php`](../docs/managenews.html#managenews)

Notes
: Since 2.1

### integrate_modify_news_settings

```php
call_integration_hook('integrate_modify_news_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ModifyNewsSettings()` in `./Sources/ManageNews.php`](../docs/managenews.html#modifynewssettings)

Notes
: Since 2.1

### integrate_save_news_settings

```php
call_integration_hook('integrate_save_news_settings')
```


Called from
: [`ModifyNewsSettings()` in `./Sources/ManageNews.php`](../docs/managenews.html#modifynewssettings)

Notes
: Since 2.1

