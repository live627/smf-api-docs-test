---
layout: default
group: hooks
title: Help
count: 2
---
* auto-gen TOC:
{:toc}

## Help.php
### integrate_manage_help

```php
call_integration_hook('integrate_manage_help', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ShowHelp()` in `./Sources/Help.php`](../docs/help.html#showhelp)

Notes
: Since 2.1

### integrate_helpadmin

```php
call_integration_hook('integrate_helpadmin')
```


Called from
: [`ShowAdminHelp()` in `./Sources/Help.php`](../docs/help.html#showadminhelp)

Notes
: Since 2.1

