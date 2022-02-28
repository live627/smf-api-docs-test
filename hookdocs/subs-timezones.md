---
layout: default
group: hooks
title: Subs-Timezones.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_metazones

```php
call_integration_hook('integrate_metazones', array(&$tzid_metazones, $when))
```

Type|Parameter|Description
---|---|---
`array`|`&$tzid_metazones`|desc
`array`|`$when`|desc

Called from
: [`get_tzid_metazones()` in `./Sources/Subs-Timezones.php`](../docs/subs-timezones.html#get_tzid_metazones)

Notes
: Since 2.1

### integrate_country_timezones

```php
call_integration_hook('integrate_country_timezones', array(&$sorted_tzids, $country_code, $when))
```

Type|Parameter|Description
---|---|---
`array`|`&$sorted_tzids`|desc
`array`|`$country_code`|desc
`array`|`$when`|desc

Called from
: [`get_sorted_tzids_for_country()` in `./Sources/Subs-Timezones.php`](../docs/subs-timezones.html#get_sorted_tzids_for_country)

Notes
: Since 2.1

### integrate_timezone_fallbacks

```php
call_integration_hook('integrate_timezone_fallbacks', array(&$fallbacks, &$missing, $tzids, $when))
```

Type|Parameter|Description
---|---|---
`array`|`&$fallbacks`|desc
`array`|`&$missing`|desc
`array`|`$tzids`|desc
`array`|`$when`|desc

Called from
: [`get_tzid_fallbacks()` in `./Sources/Subs-Timezones.php`](../docs/subs-timezones.html#get_tzid_fallbacks)

Notes
: Since 2.1

