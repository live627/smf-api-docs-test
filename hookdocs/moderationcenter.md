---
layout: default
group: hooks
title: ModerationCenter.php
count: 2
---
* auto-gen TOC:
{:toc}

## ModerationCenter.php
### integrate_mod_centre_blocks

```php
call_integration_hook('integrate_mod_centre_blocks', array(&$valid_blocks))
```

Type|Parameter|Description
---|---|---
`array`|`&$valid_blocks`|desc

Called from
: [`ModerationHome()` in `./Sources/ModerationCenter.php`](../docs/moderationcenter.html#moderationhome)

Notes
: Since 2.1

### integrate_warning_log_actions

```php
call_integration_hook('integrate_warning_log_actions', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ViewWarnings()` in `./Sources/ModerationCenter.php`](../docs/moderationcenter.html#viewwarnings)

Notes
: Since 2.1

