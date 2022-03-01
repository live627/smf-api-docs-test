---
layout: default
group: hooks
title: Reports.php
count: 4
---
* auto-gen TOC:
{:toc}

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

