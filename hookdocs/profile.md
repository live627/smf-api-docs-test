---
layout: default
group: hooks
title: Profile.php
count: 6
---
* auto-gen TOC:
{:toc}
### integrate_pre_profile_areas

```php
call_integration_hook('integrate_pre_profile_areas', array(&$profile_areas))
```

Type|Parameter|Description
---|---|---
`array`|`&$profile_areas`|desc

Called from
: [`ModifyProfile()` in `./Sources/Profile.php`](../docs/profile.html#modifyprofile)

Notes
: Since 2.1

### integrate_verify_password

```php
call_integration_hook('integrate_verify_password', array($cur_profile['member_name'], $password, false))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc
`array`|`$password`|desc
`array`|`false`|desc

Called from
: [`ModifyProfile()` in `./Sources/Profile.php`](../docs/profile.html#modifyprofile)

Notes
: Since 2.1

### integrate_profile_save

```php
call_integration_hook('integrate_profile_save', array(&$profile_vars, &$post_errors, $memID, $cur_profile, $current_area))
```

Type|Parameter|Description
---|---|---
`array`|`&$profile_vars`|desc
`array`|`&$post_errors`|desc
`array`|`$memID`|desc
`array`|`$cur_profile`|desc
`array`|`$current_area`|desc

Called from
: [`ModifyProfile()` in `./Sources/Profile.php`](../docs/profile.html#modifyprofile)

Notes
: Since 2.1

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($cur_profile['member_name'], $cur_profile['member_name'], $_POST['passwrd2']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc
`array`|`$member_name`|desc
`array`|`$passwrd2`|desc

Called from
: [`ModifyProfile()` in `./Sources/Profile.php`](../docs/profile.html#modifyprofile)

Notes
: Since 2.1

### integrate_profile_popup

```php
call_integration_hook('integrate_profile_popup', array(&$profile_items))
```

Type|Parameter|Description
---|---|---
`array`|`&$profile_items`|desc

Called from
: [`profile_popup()` in `./Sources/Profile.php`](../docs/profile.html#profile_popup)

Notes
: Since 2.1

### integrate_load_custom_profile_fields

```php
call_integration_hook('integrate_load_custom_profile_fields', array($memID, $area))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc
`array`|`$area`|desc

Called from
: [`loadCustomFields()` in `./Sources/Profile.php`](../docs/profile.html#loadcustomfields)

Notes
: Since 2.1

