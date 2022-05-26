---
layout: default
group: hooks
title: Everything in moderation
count: 8
---
* auto-gen TOC:
{:toc}
## Modlog.php
### integrate_viewModLog

```php
call_integration_hook('integrate_viewModLog', array(&$listOptions, &$moderation_menu_name))
```

Type|Parameter|Description
---|---|---
`array`|`&$listOptions`|desc
`array`|`&$moderation_menu_name`|desc

Called from
: [`ViewModlog()` in `./Sources/Modlog.php`](../docs/modlog.html#viewmodlog)

Notes
: Since 2.1

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

## PostModeration.php
### integrate_post_moderation

```php
call_integration_hook('integrate_post_moderation', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`PostModerationMain()` in `./Sources/PostModeration.php`](../docs/postmoderation.html#postmoderationmain)

Notes
: Since 2.1

## Reports.php
### integrate_report_types

```php
call_integration_hook('integrate_report_types')
```


Called from
: [`ReportsMain()` in `./Sources/Reports.php`](../docs/reports.html#reportsmain)

Notes
: Since 2.1

### integrate_report_buttons

```php
call_integration_hook('integrate_report_buttons')
```


Called from
: [`ReportsMain()` in `./Sources/Reports.php`](../docs/reports.html#reportsmain)

Notes
: Since 2.1

### integrate_reports_boardperm

```php
call_integration_hook('integrate_reports_boardperm', array(&$disabled_permissions))
```

Type|Parameter|Description
---|---|---
`array`|`&$disabled_permissions`|desc

Called from
: [`BoardPermissionsReport()` in `./Sources/Reports.php`](../docs/reports.html#boardpermissionsreport)

Notes
: Since 2.1

### integrate_reports_groupperm

```php
call_integration_hook('integrate_reports_groupperm', array(&$disabled_permissions))
```

Type|Parameter|Description
---|---|---
`array`|`&$disabled_permissions`|desc

Called from
: [`GroupPermissionsReport()` in `./Sources/Reports.php`](../docs/reports.html#grouppermissionsreport)

Notes
: Since 2.1
