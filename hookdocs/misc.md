---
layout: default
group: hooks
title: Uncategorized
count: 47
---
* auto-gen TOC:
{:toc}
## Load.php
### integrate_load_average

```php
call_integration_hook('integrate_load_average', array($modSettings['load_average']))
```

Type|Parameter|Description
---|---|---
`array`|`$load_average`|desc

Called from
: [`reloadSettings()` in `./Sources/Load.php`](../docs/load.html#reloadsettings)

Notes
: Since 2.1

### integrate_pre_load

```php
call_integration_hook('integrate_pre_load')
```


Called from
: [`reloadSettings()` in `./Sources/Load.php`](../docs/load.html#reloadsettings)

Notes
: Since 1.1

### integrate_verify_user

```php
call_integration_hook('integrate_verify_user')
```


Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 1.1

### integrate_force_tfasetup

```php
call_integration_hook('integrate_force_tfasetup', array(&$force_tfasetup))
```

Type|Parameter|Description
---|---|---
`array`|`&$force_tfasetup`|desc

Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_verify_tfa

```php
call_integration_hook('integrate_verify_tfa', array($id_member, $user_settings))
```

Type|Parameter|Description
---|---|---
`array`|`$id_member`|desc
`array`|`$user_settings`|desc

Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_user_info

```php
call_integration_hook('integrate_user_info')
```


Called from
: [`loadUserSettings()` in `./Sources/Load.php`](../docs/load.html#loadusersettings)

Notes
: Since 2.1

### integrate_load_min_user_settings_columns

```php
call_integration_hook('integrate_load_min_user_settings_columns', array(&$columns_to_load))
```

Type|Parameter|Description
---|---|---
`array`|`&$columns_to_load`|desc

Called from
: [`loadMinUserInfo()` in `./Sources/Load.php`](../docs/load.html#loadminuserinfo)

Notes
: Since 2.1

### integrate_load_min_user_settings

```php
call_integration_hook('integrate_load_min_user_settings', array(&$user_info_min))
```

Type|Parameter|Description
---|---|---
`array`|`&$user_info_min`|desc

Called from
: [`loadMinUserInfo()` in `./Sources/Load.php`](../docs/load.html#loadminuserinfo)

Notes
: Since 2.1

### integrate_load_board

```php
call_integration_hook('integrate_load_board', array(&$custom_column_selects, &$custom_column_parameters))
```

Type|Parameter|Description
---|---|---
`array`|`&$custom_column_selects`|desc
`array`|`&$custom_column_parameters`|desc

Called from
: [`loadBoard()` in `./Sources/Load.php`](../docs/load.html#loadboard)

Notes
: Since 2.1

### integrate_board_info

```php
call_integration_hook('integrate_board_info', array(&$board_info, $row))
```

Type|Parameter|Description
---|---|---
`array`|`&$board_info`|desc
`array`|`$row`|desc

Called from
: [`loadBoard()` in `./Sources/Load.php`](../docs/load.html#loadboard)

Notes
: Since 2.1

### integrate_load_member_data

```php
call_integration_hook('integrate_load_member_data', array(&$select_columns, &$select_tables, &$set))
```

Type|Parameter|Description
---|---|---
`array`|`&$select_columns`|desc
`array`|`&$select_tables`|desc
`array`|`&$set`|desc

Called from
: [`loadMemberData()` in `./Sources/Load.php`](../docs/load.html#loadmemberdata)

Notes
: Since 2.1

### integrate_member_context

```php
call_integration_hook('integrate_member_context', array(&$memberContext[$user], $user, $display_custom_fields))
```

Type|Parameter|Description
---|---|---
`array`|`&$user`|desc
`array`|`$user`|desc
`array`|`$display_custom_fields`|desc

Called from
: [`loadMemberContext()` in `./Sources/Load.php`](../docs/load.html#loadmembercontext)

Notes
: Since 2.1

### integrate_pre_load_theme

```php
call_integration_hook('integrate_pre_load_theme', array(&$id_theme))
```

Type|Parameter|Description
---|---|---
`array`|`&$id_theme`|desc

Called from
: [`loadTheme()` in `./Sources/Load.php`](../docs/load.html#loadtheme)

Notes
: Since 2.1

### integrate_simple_actions

```php
call_integration_hook('integrate_simple_actions', array(&$simpleActions, &$simpleAreas, &$simpleSubActions, &$extraParams, &$xmlActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$simpleActions`|desc
`array`|`&$simpleAreas`|desc
`array`|`&$simpleSubActions`|desc
`array`|`&$extraParams`|desc
`array`|`&$xmlActions`|desc

Called from
: [`loadTheme()` in `./Sources/Load.php`](../docs/load.html#loadtheme)

Notes
: Since 2.1

### integrate_load_theme

```php
call_integration_hook('integrate_load_theme')
```


Called from
: [`triggerCron()` in `./Sources/Load.php`](../docs/load.html#triggercron)

Notes
: Since 2.1

### pre_cache_quick_get

```php
call_integration_hook('pre_cache_quick_get', array(&$key, &$file, &$function, &$params, &$level))
```

Type|Parameter|Description
---|---|---
`array`|`&$key`|desc
`array`|`&$file`|desc
`array`|`&$function`|desc
`array`|`&$params`|desc
`array`|`&$level`|desc

Called from
: [`cache_quick_get()` in `./Sources/Load.php`](../docs/load.html#cache_quick_get)

Notes
: Since 2.1

### post_cache_quick_get

```php
call_integration_hook('post_cache_quick_get', array(&$cache_block))
```

Type|Parameter|Description
---|---|---
`array`|`&$cache_block`|desc

Called from
: [`cache_quick_get()` in `./Sources/Load.php`](../docs/load.html#cache_quick_get)

Notes
: Since 2.1

### cache_put_data

```php
call_integration_hook('cache_put_data', array(&$key, &$value, &$ttl))
```

Type|Parameter|Description
---|---|---
`array`|`&$key`|desc
`array`|`&$value`|desc
`array`|`&$ttl`|desc

Called from
: [`cache_put_data()` in `./Sources/Load.php`](../docs/load.html#cache_put_data)

Notes
: Since 2.1

### cache_get_data

```php
call_integration_hook('cache_get_data', array(&$key, &$ttl, &$value))
```

Type|Parameter|Description
---|---|---
`array`|`&$key`|desc
`array`|`&$ttl`|desc
`array`|`&$value`|desc

Called from
: [`cache_get_data()` in `./Sources/Load.php`](../docs/load.html#cache_get_data)

Notes
: Since 2.1

### integrate_clean_cache

```php
call_integration_hook('integrate_clean_cache')
```


Called from
: [`clean_cache()` in `./Sources/Load.php`](../docs/load.html#clean_cache)

Notes
: Since 2.1

### integrate_set_avatar_data

```php
call_integration_hook('integrate_set_avatar_data', array(&$image, &$data))
```

Type|Parameter|Description
---|---|---
`array`|`&$image`|desc
`array`|`&$data`|desc

Called from
: [`set_avatar_data()` in `./Sources/Load.php`](../docs/load.html#set_avatar_data)

Notes
: Since 2.1


## ScheduledTasks.php
### integrate_daily_maintenance

```php
call_integration_hook('integrate_daily_maintenance')
```


Called from
: [`scheduled_daily_maintenance()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_daily_maintenance)

Notes
: Since 2.1

### integrate_daily_digest_lang

```php
call_integration_hook('integrate_daily_digest_lang', array(&$langtxt, $lang))
```

Type|Parameter|Description
---|---|---
`array`|`&$langtxt`|desc
`array`|`$lang`|desc

Called from
: [`scheduled_daily_digest()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_daily_digest)

Notes
: Since 2.1

### integrate_daily_digest_email

```php
call_integration_hook('integrate_daily_digest_email', array(&$email, $types, $notify_types, $langtxt))
```

Type|Parameter|Description
---|---|---
`array`|`&$email`|desc
`array`|`$types`|desc
`array`|`$notify_types`|desc
`array`|`$langtxt`|desc

Called from
: [`scheduled_daily_digest()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_daily_digest)

Notes
: Since 2.1

### integrate_weekly_maintenance

```php
call_integration_hook('integrate_weekly_maintenance')
```


Called from
: [`scheduled_weekly_maintenance()` in `./Sources/ScheduledTasks.php`](../docs/scheduledtasks.html#scheduled_weekly_maintenance)

Notes
: Since 2.1

## Session.php
### integrate_load_session

```php
call_integration_hook('integrate_load_session')
```


Called from
: [`loadSession()` in `./Sources/Session.php`](../docs/session.html#loadsession)

Notes
: Since 2.1

### integrate_session_handlers

```php
call_integration_hook('integrate_session_handlers')
```


Called from
: [`loadSession()` in `./Sources/Session.php`](../docs/session.html#loadsession)

Notes
: Since 2.1

## Stats.php
### integrate_forum_stats

```php
call_integration_hook('integrate_forum_stats')
```


Called from
: [`DisplayStats()` in `./Sources/Stats.php`](../docs/stats.html#displaystats)

Notes
: Since 2.1

## Subs.php
### integrate_change_member_data

```php
call_integration_hook('integrate_change_member_data', array($member_names, $var, &$data[$var], &$knownInts, &$knownFloats))
```

Type|Parameter|Description
---|---|---
`array`|`$member_names`|desc
`array`|`$var`|desc
`array`|`&$var`|desc
`array`|`&$knownInts`|desc
`array`|`&$knownFloats`|desc

Called from
: [`updateMemberData()` in `./Sources/Subs.php`](../docs/subs.html#updatememberdata)

Notes
: Since 1.1

### integrate_pre_parsebbc

```php
call_integration_hook('integrate_pre_parsebbc', array(&$message, &$smileys, &$cache_id, &$parse_tags))
```

Type|Parameter|Description
---|---|---
`array`|`&$message`|desc
`array`|`&$smileys`|desc
`array`|`&$cache_id`|desc
`array`|`&$parse_tags`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_attach_bbc_validate

```php
call_integration_hook('integrate_attach_bbc_validate', array(&$returnContext, $currentAttachment, $tag, $data, $disabled, $params))
```

Type|Parameter|Description
---|---|---
`array`|`&$returnContext`|desc
`array`|`$currentAttachment`|desc
`array`|`$tag`|desc
`array`|`$data`|desc
`array`|`$disabled`|desc
`array`|`$params`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_bbc_codes

```php
call_integration_hook('integrate_bbc_codes', array(&$codes, &$no_autolink_tags))
```

Type|Parameter|Description
---|---|---
`array`|`&$codes`|desc
`array`|`&$no_autolink_tags`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_bbc_print

```php
call_integration_hook('integrate_bbc_print', array(&$disabled))
```

Type|Parameter|Description
---|---|---
`array`|`&$disabled`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_autolinker_schemes

```php
call_integration_hook('integrate_autolinker_schemes', array(&$schemes))
```

Type|Parameter|Description
---|---|---
`array`|`&$schemes`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_post_parsebbc

```php
call_integration_hook('integrate_post_parsebbc', array(&$message, &$smileys, &$cache_id, &$parse_tags))
```

Type|Parameter|Description
---|---|---
`array`|`&$message`|desc
`array`|`&$smileys`|desc
`array`|`&$cache_id`|desc
`array`|`&$parse_tags`|desc

Called from
: [`parse_bbc()` in `./Sources/Subs.php`](../docs/subs.html#parse_bbc)

Notes
: Since 2.1

### integrate_smileys

```php
call_integration_hook('integrate_smileys', array(&$smileyPregSearch, &$smileyPregReplacements))
```

Type|Parameter|Description
---|---|---
`array`|`&$smileyPregSearch`|desc
`array`|`&$smileyPregReplacements`|desc

Called from
: [`parsesmileys()` in `./Sources/Subs.php`](../docs/subs.html#parsesmileys)

Notes
: Since 2.1

### integrate_proxy

```php
call_integration_hook('integrate_proxy', array($url, &$proxied_url))
```

Type|Parameter|Description
---|---|---
`array`|`$url`|desc
`array`|`&$proxied_url`|desc

Called from
: [`get_proxied_url()` in `./Sources/Subs.php`](../docs/subs.html#get_proxied_url)

Notes
: Since 1.1

### integrate_redirect

```php
call_integration_hook('integrate_redirect', array(&$setLocation, &$refresh, &$permanent))
```

Type|Parameter|Description
---|---|---
`array`|`&$setLocation`|desc
`array`|`&$refresh`|desc
`array`|`&$permanent`|desc

Called from
: [`redirectexit()` in `./Sources/Subs.php`](../docs/subs.html#redirectexit)

Notes
: Since 1.1

### integrate_exit

```php
call_integration_hook('integrate_exit', array($do_footer))
```

Type|Parameter|Description
---|---|---
`array`|`$do_footer`|desc

Called from
: [`obExit()` in `./Sources/Subs.php`](../docs/subs.html#obexit)

Notes
: Since 1.1

### integrate_theme_context

```php
call_integration_hook('integrate_theme_context')
```


Called from
: [`setupThemeContext()` in `./Sources/Subs.php`](../docs/subs.html#setupthemecontext)

Notes
: Since 2.1

### integrate_security_files

```php
call_integration_hook('integrate_security_files', array(&$securityFiles))
```

Type|Parameter|Description
---|---|---
`array`|`&$securityFiles`|desc

Called from
: [`template_header()` in `./Sources/Subs.php`](../docs/subs.html#template_header)

Notes
: Since 2.1

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(&$do_deferred))
```

Type|Parameter|Description
---|---|---
`array`|`&$do_deferred`|desc

Called from
: [`template_javascript()` in `./Sources/Subs.php`](../docs/subs.html#template_javascript)

Notes
: Since 2.1

### integrate_pre_css_output

```php
call_integration_hook('integrate_pre_css_output')
```


Called from
: [`template_css()` in `./Sources/Subs.php`](../docs/subs.html#template_css)

Notes
: Since 2.1

### integrate_menu_buttons

```php
call_integration_hook('integrate_menu_buttons', array(&$buttons))
```

Type|Parameter|Description
---|---|---
`array`|`&$buttons`|desc

Called from
: [`setupMenuContext()` in `./Sources/Subs.php`](../docs/subs.html#setupmenucontext)

Notes
: Since 2.1

### integrate_current_action

```php
call_integration_hook('integrate_current_action', array(&$current_action))
```

Type|Parameter|Description
---|---|---
`array`|`&$current_action`|desc

Called from
: [`setupMenuContext()` in `./Sources/Subs.php`](../docs/subs.html#setupmenucontext)

Notes
: Since 2.1

