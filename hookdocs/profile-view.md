---
layout: default
group: hooks
title: Profile-View.php
count: 4
---
* auto-gen TOC:
{:toc}
### integrate_fetch_alerts

```php
call_integration_hook('integrate_fetch_alerts', array(&$alerts, &$formats))
```

Type|Parameter|Description
---|---|---
`array`|`$&alerts`|desc
`array`|`$&formats`|desc

Called from
: [`fetch_alerts()` in `./Sources/Profile-View.php`](../docs/profile-view.html#fetch_alerts)

Notes
: Since 2.1

### integrate_profile_showPosts

```php
call_integration_hook('integrate_profile_showPosts')
```


Called from
: [`showPosts()` in `./Sources/Profile-View.php`](../docs/profile-view.html#showposts)

Notes
: Since 2.1

### integrate_profile_stats

```php
call_integration_hook('integrate_profile_stats', array($memID, &$context['text_stats']))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc
`array`|`$&text_stats`|desc

Called from
: [`statPanel()` in `./Sources/Profile-View.php`](../docs/profile-view.html#statpanel)

Notes
: Since 2.1

### integrate_profile_trackip

```php
call_integration_hook('integrate_profile_trackip', array($ip_string, $ip_var))
```

Type|Parameter|Description
---|---|---
`array`|`$ip_string`|desc
`array`|`$ip_var`|desc

Called from
: [`TrackIP()` in `./Sources/Profile-View.php`](../docs/profile-view.html#trackip)

Notes
: Since 2.1

