---
layout: default
group: hooks
title: Members
count: 48
---
{:toc}
## Groups.php
### integrate_manage_groups

```php
call_integration_hook('integrate_manage_groups', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`Groups()` in `./Sources/Groups.php`](../docs/groups.html#groups)

Notes
: Since 2.1

## Memberlist.php
### integrate_memberlist_buttons

```php
call_integration_hook('integrate_memberlist_buttons')
```

Called from
: [`Memberlist()` in `./Sources/Memberlist.php`](../docs/memberlist.html#memberlist)

Notes
: Since 2.1
## Profile.php
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


## Profile-Actions.php
### integrate_activate

```php
call_integration_hook('integrate_activate', array($user_profile[$memID]['member_name']))
```

Type|Parameter|Description
---|---|---
`array`|`$memID['member_name']`|desc

Called from
: [`activateAccount()` in `./Sources/Profile-Actions.php`](../docs/profile-actions.html#activateaccount)

Notes
: Since 2.1


## Profile-Export.php
### integrate_export_xslt_variables

```php
call_integration_hook('integrate_export_xslt_variables', array(&$xslt_variables, $format))
```

Type|Parameter|Description
---|---|---
`array`|`&$xslt_variables`|desc
`array`|`$format`|desc

Called from
: [`get_xslt_stylesheet()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#get_xslt_stylesheet)

Notes
: Since 2.1

### integrate_export_xslt_stylesheet

```php
call_integration_hook('integrate_export_xslt_stylesheet', array(&$stylesheet, $format))
```

Type|Parameter|Description
---|---|---
`array`|`&$stylesheet`|desc
`array`|`$format`|desc

Called from
: [`get_xslt_stylesheet()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#get_xslt_stylesheet)

Notes
: Since 2.1

### integrate_pre_css_output

```php
call_integration_hook('integrate_pre_css_output')
```


Called from
: [`export_load_css_js()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#export_load_css_js)

Notes
: Since 2.1

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(true))
```

Type|Parameter|Description
---|---|---
`array`|`true`|desc

Called from
: [`export_load_css_js()` in `./Sources/Profile-Export.php`](../docs/profile-export.html#export_load_css_js)

Notes
: Since 2.1


## Profile-Modify.php
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
`array`|`&$profile_fields`|desc

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
`array`|`&$fields`|desc

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
`array`|`&$changes`|desc
`array`|`&$log_changes`|desc
`array`|`&$errors`|desc
`array`|`$returnErrors`|desc
`array`|`$memID`|desc
`array`|`$area`|desc
`array`|`$sanitize`|desc
`array`|`&$deletes`|desc

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
`array`|`&$new_buddies`|desc

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
`array`|`&$alert_types`|desc
`array`|`&$group_options`|desc

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
`array`|`&$value`|desc

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


## Profile-View.php
### integrate_fetch_alerts

```php
call_integration_hook('integrate_fetch_alerts', array(&$alerts, &$formats))
```

Type|Parameter|Description
---|---|---
`array`|`&$alerts`|desc
`array`|`&$formats`|desc

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
`array`|`&$text_stats`|desc

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


## Register.php
### integrate_activate

```php
call_integration_hook('integrate_activate', array($regOptions['username']))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc

Called from
: [`Register2()` in `./Sources/Register.php`](../docs/register.html#register2)

Notes
: Since 2.1

### integrate_activate

```php
call_integration_hook('integrate_activate', array($row['member_name']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc

Called from
: [`Activate()` in `./Sources/Register.php`](../docs/register.html#activate)

Notes
: Since 2.1


## Reminder.php
### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($username, $username, $_POST['passwrd1']))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc
`array`|`$username`|desc
`array`|`$passwrd1`|desc

Called from
: [`setPassword2()` in `./Sources/Reminder.php`](../docs/reminder.html#setpassword2)

Notes
: Since 2.1

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($row['member_name'], $row['member_name'], $_POST['passwrd1']))
```

Type|Parameter|Description
---|---|---
`array`|`$member_name`|desc
`array`|`$member_name`|desc
`array`|`$passwrd1`|desc

Called from
: [`SecretAnswer2()` in `./Sources/Reminder.php`](../docs/reminder.html#secretanswer2)

Notes
: Since 2.1

## Subs-Membergroups.php
### integrate_delete_membergroups

```php
call_integration_hook('integrate_delete_membergroups', array($groups))
```

Type|Parameter|Description
---|---|---
`array`|`$groups`|desc

Called from
: [`deleteMembergroups()` in `./Sources/Subs-Membergroups.php`](../docs/subs-membergroups.html#deletemembergroups)

Notes
: Since 2.1

### integrate_add_members_to_group

```php
call_integration_hook('integrate_add_members_to_group', array($members, $group, &$group_names))
```

Type|Parameter|Description
---|---|---
`array`|`$members`|desc
`array`|`$group`|desc
`array`|`&$group_names`|desc

Called from
: [`addMembersToGroup()` in `./Sources/Subs-Membergroups.php`](../docs/subs-membergroups.html#addmemberstogroup)

Notes
: Since 2.1

### integrate_getMembergroupList

```php
call_integration_hook('integrate_getMembergroupList', array(&$groupCache, $group))
```

Type|Parameter|Description
---|---|---
`array`|`&$groupCache`|desc
`array`|`$group`|desc

Called from
: [`cache_getMembergroupList()` in `./Sources/Subs-Membergroups.php`](../docs/subs-membergroups.html#cache_getmembergrouplist)

Notes
: Since 2.1

## Subs-Members.php
### integrate_delete_members

```php
call_integration_hook('integrate_delete_members', array($users))
```

Type|Parameter|Description
---|---|---
`array`|`$users`|desc

Called from
: [`deleteMembers()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#deletemembers)

Notes
: Since 2.1

### integrate_register_check

```php
call_integration_hook('integrate_register_check', array(&$regOptions, &$reg_errors))
```

Type|Parameter|Description
---|---|---
`array`|`&$regOptions`|desc
`array`|`&$reg_errors`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_register

```php
call_integration_hook('integrate_register', array(&$regOptions, &$theme_vars, &$knownInts, &$knownFloats))
```

Type|Parameter|Description
---|---|---
`array`|`&$regOptions`|desc
`array`|`&$theme_vars`|desc
`array`|`&$knownInts`|desc
`array`|`&$knownFloats`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_post_register

```php
call_integration_hook('integrate_post_register', array(&$regOptions, &$theme_vars, &$memberID))
```

Type|Parameter|Description
---|---|---
`array`|`&$regOptions`|desc
`array`|`&$theme_vars`|desc
`array`|`&$memberID`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_register_after

```php
call_integration_hook('integrate_register_after', array($regOptions, $memberID))
```

Type|Parameter|Description
---|---|---
`array`|`$regOptions`|desc
`array`|`$memberID`|desc

Called from
: [`registerMember()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#registermember)

Notes
: Since 2.1

### integrate_check_name

```php
call_integration_hook('integrate_check_name', array($checkName, &$is_reserved, $current_id_member, $is_name))
```

Type|Parameter|Description
---|---|---
`array`|`$checkName`|desc
`array`|`&$is_reserved`|desc
`array`|`$current_id_member`|desc
`array`|`$is_name`|desc

Called from
: [`isReservedName()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#isreservedname)

Notes
: Since 2.1

### integrate_groups_allowed_to

```php
call_integration_hook('integrate_groups_allowed_to', array(&$member_groups, $permission, $board_id))
```

Type|Parameter|Description
---|---|---
`array`|`&$member_groups`|desc
`array`|`$permission`|desc
`array`|`$board_id`|desc

Called from
: [`groupsAllowedTo()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#groupsallowedto)

Notes
: Since 2.1

### integrate_reattribute_posts

```php
call_integration_hook('integrate_reattribute_posts', array($memID, $email, $membername, $post_count, &$updated))
```

Type|Parameter|Description
---|---|---
`array`|`$memID`|desc
`array`|`$email`|desc
`array`|`$membername`|desc
`array`|`$post_count`|desc
`array`|`&$updated`|desc

Called from
: [`reattributePosts()` in `./Sources/Subs-Members.php`](../docs/subs-members.html#reattributeposts)

Notes
: Since 2.1

## Subs-MembersOnline.php
### integrate_online_stats

```php
call_integration_hook('integrate_online_stats', array(&$membersOnlineStats))
```

Type|Parameter|Description
---|---|---
`array`|`&$membersOnlineStats`|desc

Called from
: [`getMembersOnlineStats()` in `./Sources/Subs-MembersOnline.php`](../docs/subs-membersonline.html#getmembersonlinestats)

Notes
: Since 2.1

## Subs-Timezones.php
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

