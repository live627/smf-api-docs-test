---
layout: default
group: hooks
title: Profile-Modify.php
count: 12
---
* auto-gen TOC:
{:toc}
### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($cur_profile['member_name'], $value, $_POST['passwrd1']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc
`array`|`$value`|desc
`array`|`$passwrd1`|desc

Called from
: [`loadProfileFields()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#loadprofilefields)

Notes
: Since 2.1

### integrate_load_profile_fields

```php
call_integration_hook('integrate_load_profile_fields', array(&$profile_fields))
```

Type|Parameter|Description
---|---|---
`array`|`$&profile_fields`|desc

Called from
: [`loadProfileFields()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#loadprofilefields)

Notes
: Since 2.1

### integrate_setup_profile_context

```php
call_integration_hook('integrate_setup_profile_context', array(&$fields))
```

Type|Parameter|Description
---|---|---
`array`|`$&fields`|desc

Called from
: [`setupProfileContext()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#setupprofilecontext)

Notes
: Since 2.1

### integrate_save_custom_profile_fields

```php
call_integration_hook('integrate_save_custom_profile_fields', array(&$changes, &$log_changes, &$errors, $returnErrors, $memID, $area, $sanitize, &$deletes))
```

Type|Parameter|Description
---|---|---
`array`|`$&changes`|desc
`array`|`$&log_changes`|desc
`array`|`$&errors`|desc
`array`|`$returnErrors`|desc
`array`|`$memID`|desc
`array`|`$area`|desc
`array`|`$sanitize`|desc
`array`|`$&deletes`|desc

Called from
: [`makeCustomFieldChanges()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#makecustomfieldchanges)

Notes
: Since 2.1

### integrate_remove_buddy

```php
call_integration_hook('integrate_remove_buddy', array($memID))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc

Called from
: [`editBuddies()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#editbuddies)

Notes
: Since 2.1

### integrate_add_buddies

```php
call_integration_hook('integrate_add_buddies', array($memID, &$new_buddies))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc
`array`|`$&new_buddies`|desc

Called from
: [`editBuddies()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#editbuddies)

Notes
: Since 2.1

### integrate_view_buddies

```php
call_integration_hook('integrate_view_buddies', array($memID))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc

Called from
: [`editBuddies()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#editbuddies)

Notes
: Since 2.1

### integrate_theme_options

```php
call_integration_hook('integrate_theme_options')
```


Called from
: [`theme()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#theme)

Notes
: Since 2.1

### integrate_alert_types

```php
call_integration_hook('integrate_alert_types', array(&$alert_types, &$group_options))
```

Type|Parameter|Description
---|---|---
`array`|`$&alert_types`|desc
`array`|`$&group_options`|desc

Called from
: [`alert_configuration()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#alert_configuration)

Notes
: Since 2.1

### integrate_profile_profileSaveGroups

```php
call_integration_hook('integrate_profile_profileSaveGroups', array($value, $additional_groups))
```

Type|Parameter|Description
---|---|---
`array`|`$value`|desc
`array`|`$additional_groups`|desc

Called from
: [`profileSaveGroups()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#profilesavegroups)

Notes
: Since 2.1

### before_profile_save_avatar

```php
call_integration_hook('before_profile_save_avatar', array(&$value))
```

Type|Parameter|Description
---|---|---
`array`|`$&value`|desc

Called from
: [`profileSaveAvatarData()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#profilesaveavatardata)

Notes
: Since 2.1

### after_profile_save_avatar

```php
call_integration_hook('after_profile_save_avatar')
```


Called from
: [`profileSaveAvatarData()` in `./Sources/Profile-Modify.php`](../docs/profile-modify.html#profilesaveavatardata)

Notes
: Since 2.1

