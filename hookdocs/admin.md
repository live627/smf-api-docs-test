---
layout: default
group: hooks
title: Admin.php
count: 2
---
* auto-gen TOC:
{:toc}

## Admin.php
### integrate_admin_search

```php
call_integration_hook('integrate_admin_search', array(&$language_files, &$include_files, &$settings_search))
```

Type|Parameter|Description
---|---|---
`array`|`&$language_files`|desc
`array`|`&$include_files`|desc
`array`|`&$settings_search`|desc

Called from
: [`AdminSearchInternal()` in `./Sources/Admin.php`](../docs/admin.html#adminsearchinternal)

Notes
: Since 2.1

### integrate_manage_logs

```php
call_integration_hook('integrate_manage_logs', array(&$log_functions))
```

Type|Parameter|Description
---|---|---
`array`|`&$log_functions`|desc

Called from
: [`AdminLogs()` in `./Sources/Admin.php`](../docs/admin.html#adminlogs)

Notes
: Since 2.1


## ManageAttachments.php
### integrate_manage_attachments

```php
call_integration_hook('integrate_manage_attachments', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageattachments)

Notes
: Since 2.1

### integrate_modify_attachment_settings

```php
call_integration_hook('integrate_modify_attachment_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ManageAttachmentSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageattachmentsettings)

Notes
: Since 2.1

### integrate_save_attachment_settings

```php
call_integration_hook('integrate_save_attachment_settings')
```


Called from
: [`ManageAttachmentSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageattachmentsettings)

Notes
: Since 2.1

### integrate_modify_avatar_settings

```php
call_integration_hook('integrate_modify_avatar_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ManageAvatarSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageavatarsettings)

Notes
: Since 2.1

### integrate_save_avatar_settings

```php
call_integration_hook('integrate_save_avatar_settings')
```


Called from
: [`ManageAvatarSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageavatarsettings)

Notes
: Since 2.1

### integrate_attachments_browse

```php
call_integration_hook('integrate_attachments_browse', array(&$listOptions, &$titles, &$list_title))
```

Type|Parameter|Description
---|---|---
`array`|`&$listOptions`|desc
`array`|`&$titles`|desc
`array`|`&$list_title`|desc

Called from
: [`BrowseFiles()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#browsefiles)

Notes
: Since 2.1

### integrate_attachment_remove

```php
call_integration_hook('integrate_attachment_remove', array(&$filesRemoved, $attachments))
```

Type|Parameter|Description
---|---|---
`array`|`&$filesRemoved`|desc
`array`|`$attachments`|desc

Called from
: [`RemoveAttachment()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#removeattachment)

Notes
: Since 2.1

### integrate_remove_attachments

```php
call_integration_hook('integrate_remove_attachments', array($attach))
```

Type|Parameter|Description
---|---|---
`array`|`$attach`|desc

Called from
: [`removeAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#removeattachments)

Notes
: Since 2.1

### integrate_repair_attachments_nomsg

```php
call_integration_hook('integrate_repair_attachments_nomsg', array(&$ignore_ids, $_GET['substep'], $_GET['substep'] + 500))
```

Type|Parameter|Description
---|---|---
`array`|`&$ignore_ids`|desc
`array`|`$substep`|desc
`array`|`$substep + 500`|desc

Called from
: [`RepairAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#repairattachments)

Notes
: Since 2.1

### integrate_approve_attachments

```php
call_integration_hook('integrate_approve_attachments', array($attachments))
```

Type|Parameter|Description
---|---|---
`array`|`$attachments`|desc

Called from
: [`ApproveAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#approveattachments)

Notes
: Since 2.1


## ManageBans.php
### integrate_manage_bans

```php
call_integration_hook('integrate_manage_bans', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`Ban()` in `./Sources/ManageBans.php`](../docs/managebans.html#ban)

Notes
: Since 2.1

### integrate_ban_edit_list

```php
call_integration_hook('integrate_ban_edit_list', array(&$listOptions))
```

Type|Parameter|Description
---|---|---
`array`|`&$listOptions`|desc

Called from
: [`BanEdit()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit)

Notes
: Since 2.1

### integrate_ban_edit_new

```php
call_integration_hook('integrate_ban_edit_new')
```


Called from
: [`BanEdit()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit)

Notes
: Since 2.1

### integrate_ban_list

```php
call_integration_hook('integrate_ban_list', array(&$ban_items))
```

Type|Parameter|Description
---|---|---
`array`|`&$ban_items`|desc

Called from
: [`list_getBanItems()` in `./Sources/ManageBans.php`](../docs/managebans.html#list_getbanitems)

Notes
: Since 2.1

### integrate_load_addtional_ip_ban

```php
call_integration_hook('integrate_load_addtional_ip_ban', array(&$search_list))
```

Type|Parameter|Description
---|---|---
`array`|`&$search_list`|desc

Called from
: [`banLoadAdditionalIPs()` in `./Sources/ManageBans.php`](../docs/managebans.html#banloadadditionalips)

Notes
: Since 2.1

### integrate_edit_bans

```php
call_integration_hook('integrate_edit_bans', array(&$ban_info, empty($_REQUEST['bg']))
```

Type|Parameter|Description
---|---|---
`array`|`&$ban_info`|desc
`array`|`empty($bg`|desc

Called from
: [`banEdit2()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit2)

Notes
: Since 2.1

### integrate_edit_bans_post

```php
call_integration_hook('integrate_edit_bans_post')
```


Called from
: [`banEdit2()` in `./Sources/ManageBans.php`](../docs/managebans.html#banedit2)

Notes
: Since 2.1

### integrate_save_triggers

```php
call_integration_hook('integrate_save_triggers', array(&$ban_triggers, &$ban_group))
```

Type|Parameter|Description
---|---|---
`array`|`&$ban_triggers`|desc
`array`|`&$ban_group`|desc

Called from
: [`saveTriggers()` in `./Sources/ManageBans.php`](../docs/managebans.html#savetriggers)

Notes
: Since 2.1

### integrate_remove_triggers

```php
call_integration_hook('integrate_remove_triggers', array(&$items_ids, $group_id))
```

Type|Parameter|Description
---|---|---
`array`|`&$items_ids`|desc
`array`|`$group_id`|desc

Called from
: [`removeBanTriggers()` in `./Sources/ManageBans.php`](../docs/managebans.html#removebantriggers)

Notes
: Since 2.1


## ManageBoards.php
### integrate_manage_boards

```php
call_integration_hook('integrate_manage_boards', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageBoards()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#manageboards)

Notes
: Since 2.1

### integrate_boards_main

```php
call_integration_hook('integrate_boards_main')
```


Called from
: [`ManageBoardsMain()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#manageboardsmain)

Notes
: Since 2.1

### integrate_edit_category

```php
call_integration_hook('integrate_edit_category')
```


Called from
: [`EditCategory()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editcategory)

Notes
: Since 2.1

### integrate_edit_board

```php
call_integration_hook('integrate_edit_board')
```


Called from
: [`EditBoard()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editboard)

Notes
: Since 2.1

### integrate_modify_board_settings

```php
call_integration_hook('integrate_modify_board_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`EditBoardSettings()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editboardsettings)

Notes
: Since 2.1

### integrate_save_board_settings

```php
call_integration_hook('integrate_save_board_settings')
```


Called from
: [`EditBoardSettings()` in `./Sources/ManageBoards.php`](../docs/manageboards.html#editboardsettings)

Notes
: Since 2.1


## ManageCalendar.php
### integrate_manage_calendar

```php
call_integration_hook('integrate_manage_calendar', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageCalendar()` in `./Sources/ManageCalendar.php`](../docs/managecalendar.html#managecalendar)

Notes
: Since 2.1

### integrate_modify_calendar_settings

```php
call_integration_hook('integrate_modify_calendar_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyCalendarSettings()` in `./Sources/ManageCalendar.php`](../docs/managecalendar.html#modifycalendarsettings)

Notes
: Since 2.1

### integrate_save_calendar_settings

```php
call_integration_hook('integrate_save_calendar_settings')
```


Called from
: [`ModifyCalendarSettings()` in `./Sources/ManageCalendar.php`](../docs/managecalendar.html#modifycalendarsettings)

Notes
: Since 2.1


## ManageLanguages.php
### integrate_manage_languages

```php
call_integration_hook('integrate_manage_languages', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageLanguages()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#managelanguages)

Notes
: Since 2.1

### integrate_language_settings

```php
call_integration_hook('integrate_language_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyLanguageSettings()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguagesettings)

Notes
: Since 2.1

### integrate_save_language_settings

```php
call_integration_hook('integrate_save_language_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyLanguageSettings()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguagesettings)

Notes
: Since 2.1

### integrate_modifylanguages

```php
call_integration_hook('integrate_modifylanguages', array(&$themes, &$lang_dirs, &$allows_add_remove, &$additional_string_types))
```

Type|Parameter|Description
---|---|---
`array`|`&$themes`|desc
`array`|`&$lang_dirs`|desc
`array`|`&$allows_add_remove`|desc
`array`|`&$additional_string_types`|desc

Called from
: [`ModifyLanguage()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguage)

Notes
: Since 2.1

### integrate_language_edit_helptext

```php
call_integration_hook('integrate_language_edit_helptext', array(&$special_groups))
```

Type|Parameter|Description
---|---|---
`array`|`&$special_groups`|desc

Called from
: [`ModifyLanguage()` in `./Sources/ManageLanguages.php`](../docs/managelanguages.html#modifylanguage)

Notes
: Since 2.1


## ManageMail.php
### integrate_manage_mail

```php
call_integration_hook('integrate_manage_mail', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageMail()` in `./Sources/ManageMail.php`](../docs/managemail.html#managemail)

Notes
: Since 2.1

### integrate_modify_mail_settings

```php
call_integration_hook('integrate_modify_mail_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyMailSettings()` in `./Sources/ManageMail.php`](../docs/managemail.html#modifymailsettings)

Notes
: Since 2.1

### integrate_save_mail_settings

```php
call_integration_hook('integrate_save_mail_settings')
```


Called from
: [`ModifyMailSettings()` in `./Sources/ManageMail.php`](../docs/managemail.html#modifymailsettings)

Notes
: Since 2.1


## ManageMaintenance.php
### integrate_manage_maintenance

```php
call_integration_hook('integrate_manage_maintenance', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageMaintenance()` in `./Sources/ManageMaintenance.php`](../docs/managemaintenance.html#managemaintenance)

Notes
: Since 2.1

### integrate_convert_msgbody

```php
call_integration_hook('integrate_convert_msgbody', array($body_type))
```

Type|Parameter|Description
---|---|---
`array`|`$body_type`|desc

Called from
: [`ConvertMsgBody()` in `./Sources/ManageMaintenance.php`](../docs/managemaintenance.html#convertmsgbody)

Notes
: Since 2.1


## ManageMembergroups.php
### integrate_manage_membergroups

```php
call_integration_hook('integrate_manage_membergroups', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ModifyMembergroups()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#modifymembergroups)

Notes
: Since 2.1

### integrate_pre_add_membergroup

```php
call_integration_hook('integrate_pre_add_membergroup')
```


Called from
: [`AddMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#addmembergroup)

Notes
: Since 2.1

### integrate_add_membergroup

```php
call_integration_hook('integrate_add_membergroup', array($id_group, $postCountBasedGroup))
```

Type|Parameter|Description
---|---|---
`array`|`$id_group`|desc
`array`|`$postCountBasedGroup`|desc

Called from
: [`AddMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#addmembergroup)

Notes
: Since 2.1

### integrate_save_membergroup

```php
call_integration_hook('integrate_save_membergroup', array((int))
```

Type|Parameter|Description
---|---|---
`array`|`(int`|desc

Called from
: [`EditMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#editmembergroup)

Notes
: Since 2.1

### integrate_view_membergroup

```php
call_integration_hook('integrate_view_membergroup')
```


Called from
: [`EditMembergroup()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#editmembergroup)

Notes
: Since 2.1

### integrate_modify_membergroup_settings

```php
call_integration_hook('integrate_modify_membergroup_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyMembergroupsettings()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#modifymembergroupsettings)

Notes
: Since 2.1

### integrate_save_membergroup_settings

```php
call_integration_hook('integrate_save_membergroup_settings')
```


Called from
: [`ModifyMembergroupsettings()` in `./Sources/ManageMembergroups.php`](../docs/managemembergroups.html#modifymembergroupsettings)

Notes
: Since 2.1


## ManageMembers.php
### integrate_manage_members

```php
call_integration_hook('integrate_manage_members', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ViewMembers()` in `./Sources/ManageMembers.php`](../docs/managemembers.html#viewmembers)

Notes
: Since 2.1

### integrate_view_members_params

```php
call_integration_hook('integrate_view_members_params', array(&$params))
```

Type|Parameter|Description
---|---|---
`array`|`&$params`|desc

Called from
: [`ViewMemberlist()` in `./Sources/ManageMembers.php`](../docs/managemembers.html#viewmemberlist)

Notes
: Since 2.1

### integrate_activate

```php
call_integration_hook('integrate_activate', array($member['username']))
```

Type|Parameter|Description
---|---|---
`array`|`$username`|desc

Called from
: [`AdminApprove()` in `./Sources/ManageMembers.php`](../docs/managemembers.html#adminapprove)

Notes
: Since 2.1


## ManageNews.php
### integrate_manage_news

```php
call_integration_hook('integrate_manage_news', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageNews()` in `./Sources/ManageNews.php`](../docs/managenews.html#managenews)

Notes
: Since 2.1

### integrate_modify_news_settings

```php
call_integration_hook('integrate_modify_news_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyNewsSettings()` in `./Sources/ManageNews.php`](../docs/managenews.html#modifynewssettings)

Notes
: Since 2.1

### integrate_save_news_settings

```php
call_integration_hook('integrate_save_news_settings')
```


Called from
: [`ModifyNewsSettings()` in `./Sources/ManageNews.php`](../docs/managenews.html#modifynewssettings)

Notes
: Since 2.1


## ManagePaid.php
### integrate_manage_subscriptions

```php
call_integration_hook('integrate_manage_subscriptions', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManagePaidSubscriptions()` in `./Sources/ManagePaid.php`](../docs/managepaid.html#managepaidsubscriptions)

Notes
: Since 2.1

### integrate_delete_subscription

```php
call_integration_hook('integrate_delete_subscription', array($context['sub_id']))
```

Type|Parameter|Description
---|---|---
`array`|`$sub_id`|desc

Called from
: [`ModifySubscription()` in `./Sources/ManagePaid.php`](../docs/managepaid.html#modifysubscription)

Notes
: Since 2.1

### integrate_save_subscription

```php
call_integration_hook('integrate_save_subscription', array(($context['action_type'] == 'add' ? $id_subscribe : $context['sub_id']))
```

Type|Parameter|Description
---|---|---
`array`|`???`|desc

Called from
: [`ModifySubscription()` in `./Sources/ManagePaid.php`](../docs/managepaid.html#modifysubscription)

Notes
: Since 2.1


## ManagePermissions.php
### integrate_manage_permissions

```php
call_integration_hook('integrate_manage_permissions', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ModifyPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#modifypermissions)

Notes
: Since 2.1

### integrate_modify_permission_settings

```php
call_integration_hook('integrate_modify_permission_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`GeneralPermissionSettings()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#generalpermissionsettings)

Notes
: Since 2.1

### integrate_save_permission_settings

```php
call_integration_hook('integrate_save_permission_settings')
```


Called from
: [`GeneralPermissionSettings()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#generalpermissionsettings)

Notes
: Since 2.1

### integrate_load_permission_levels

```php
call_integration_hook('integrate_load_permission_levels', array(&$groupLevels, &$boardLevels))
```

Type|Parameter|Description
---|---|---
`array`|`&$groupLevels`|desc
`array`|`&$boardLevels`|desc

Called from
: [`setPermissionLevel()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#setpermissionlevel)

Notes
: Since 2.1

### integrate_load_permissions

```php
call_integration_hook('integrate_load_permissions', array(&$permissionGroups, &$permissionList, &$leftPermissionGroups, &$hiddenPermissions, &$relabelPermissions))
```

Type|Parameter|Description
---|---|---
`array`|`&$permissionGroups`|desc
`array`|`&$permissionList`|desc
`array`|`&$leftPermissionGroups`|desc
`array`|`&$hiddenPermissions`|desc
`array`|`&$relabelPermissions`|desc

Called from
: [`loadAllPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#loadallpermissions)

Notes
: Since 2.1

### integrate_load_illegal_permissions

```php
call_integration_hook('integrate_load_illegal_permissions')
```


Called from
: [`loadIllegalPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#loadillegalpermissions)

Notes
: Since 2.1

### integrate_load_illegal_guest_permissions

```php
call_integration_hook('integrate_load_illegal_guest_permissions')
```


Called from
: [`loadIllegalGuestPermissions()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#loadillegalguestpermissions)

Notes
: Since 2.1

### integrate_post_moderation_mapping

```php
call_integration_hook('integrate_post_moderation_mapping', array(&$mappings))
```

Type|Parameter|Description
---|---|---
`array`|`&$mappings`|desc

Called from
: [`ModifyPostModeration()` in `./Sources/ManagePermissions.php`](../docs/managepermissions.html#modifypostmoderation)

Notes
: Since 2.1


## ManagePosts.php
### integrate_manage_posts

```php
call_integration_hook('integrate_manage_posts', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManagePostSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#managepostsettings)

Notes
: Since 2.1

### integrate_save_censors

```php
call_integration_hook('integrate_save_censors', array(&$updates))
```

Type|Parameter|Description
---|---|---
`array`|`&$updates`|desc

Called from
: [`SetCensor()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#setcensor)

Notes
: Since 2.1

### integrate_censors

```php
call_integration_hook('integrate_censors')
```


Called from
: [`SetCensor()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#setcensor)

Notes
: Since 2.1

### integrate_modify_post_settings

```php
call_integration_hook('integrate_modify_post_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyPostSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifypostsettings)

Notes
: Since 2.1

### integrate_save_post_settings

```php
call_integration_hook('integrate_save_post_settings')
```


Called from
: [`ModifyPostSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifypostsettings)

Notes
: Since 2.1

### integrate_modify_topic_settings

```php
call_integration_hook('integrate_modify_topic_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyTopicSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifytopicsettings)

Notes
: Since 2.1

### integrate_save_topic_settings

```php
call_integration_hook('integrate_save_topic_settings')
```


Called from
: [`ModifyTopicSettings()` in `./Sources/ManagePosts.php`](../docs/manageposts.html#modifytopicsettings)

Notes
: Since 2.1


## ManageRegistration.php
### integrate_manage_registrations

```php
call_integration_hook('integrate_manage_registrations', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`RegCenter()` in `./Sources/ManageRegistration.php`](../docs/manageregistration.html#regcenter)

Notes
: Since 2.1

### integrate_modify_registration_settings

```php
call_integration_hook('integrate_modify_registration_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyRegistrationSettings()` in `./Sources/ManageRegistration.php`](../docs/manageregistration.html#modifyregistrationsettings)

Notes
: Since 2.1

### integrate_save_registration_settings

```php
call_integration_hook('integrate_save_registration_settings')
```


Called from
: [`ModifyRegistrationSettings()` in `./Sources/ManageRegistration.php`](../docs/manageregistration.html#modifyregistrationsettings)

Notes
: Since 2.1


## ManageScheduledTasks.php
### integrate_manage_scheduled_tasks

```php
call_integration_hook('integrate_manage_scheduled_tasks', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageScheduledTasks()` in `./Sources/ManageScheduledTasks.php`](../docs/managescheduledtasks.html#managescheduledtasks)

Notes
: Since 2.1

### integrate_scheduled_tasks_settings

```php
call_integration_hook('integrate_scheduled_tasks_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`TaskSettings()` in `./Sources/ManageScheduledTasks.php`](../docs/managescheduledtasks.html#tasksettings)

Notes
: Since 2.1

### integrate_save_scheduled_tasks_settings

```php
call_integration_hook('integrate_save_scheduled_tasks_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$save_vars`|desc

Called from
: [`TaskSettings()` in `./Sources/ManageScheduledTasks.php`](../docs/managescheduledtasks.html#tasksettings)

Notes
: Since 2.1


## ManageSearch.php
### integrate_manage_search

```php
call_integration_hook('integrate_manage_search', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageSearch()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#managesearch)

Notes
: Since 2.1

### integrate_modify_search_settings

```php
call_integration_hook('integrate_modify_search_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`EditSearchSettings()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editsearchsettings)

Notes
: Since 2.1

### integrate_save_search_settings

```php
call_integration_hook('integrate_save_search_settings')
```


Called from
: [`EditSearchSettings()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editsearchsettings)

Notes
: Since 2.1

### integrate_modify_search_weights

```php
call_integration_hook('integrate_modify_search_weights', array(&$factors))
```

Type|Parameter|Description
---|---|---
`array`|`&$factors`|desc

Called from
: [`EditWeights()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editweights)

Notes
: Since 2.1

### integrate_save_search_weights

```php
call_integration_hook('integrate_save_search_weights')
```


Called from
: [`EditWeights()` in `./Sources/ManageSearch.php`](../docs/managesearch.html#editweights)

Notes
: Since 2.1


## ManageSearchEngines.php
### integrate_manage_search_engines

```php
call_integration_hook('integrate_manage_search_engines', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`SearchEngines()` in `./Sources/ManageSearchEngines.php`](../docs/managesearchengines.html#searchengines)

Notes
: Since 2.1

### integrate_modify_search_engine_settings

```php
call_integration_hook('integrate_modify_search_engine_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`disableFields()` in `./Sources/ManageSearchEngines.php`](../docs/managesearchengines.html#disablefields)

Notes
: Since 2.1

### integrate_save_search_engine_settings

```php
call_integration_hook('integrate_save_search_engine_settings')
```


Called from
: [`disableFields()` in `./Sources/ManageSearchEngines.php`](../docs/managesearchengines.html#disablefields)

Notes
: Since 2.1


## ManageServer.php
### integrate_server_settings

```php
call_integration_hook('integrate_server_settings', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ModifySettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifysettings)

Notes
: Since 2.1

### integrate_general_settings

```php
call_integration_hook('integrate_general_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyGeneralSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsettings)

Notes
: Since 2.1

### integrate_save_general_settings

```php
call_integration_hook('integrate_save_general_settings')
```


Called from
: [`ModifyGeneralSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsettings)

Notes
: Since 2.1

### integrate_database_settings

```php
call_integration_hook('integrate_database_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyDatabaseSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifydatabasesettings)

Notes
: Since 2.1

### integrate_save_database_settings

```php
call_integration_hook('integrate_save_database_settings')
```


Called from
: [`ModifyDatabaseSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifydatabasesettings)

Notes
: Since 2.1

### integrate_cookie_settings

```php
call_integration_hook('integrate_cookie_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`hideGlobalCookies()` in `./Sources/ManageServer.php`](../docs/manageserver.html#hideglobalcookies)

Notes
: Since 2.1

### integrate_save_cookie_settings

```php
call_integration_hook('integrate_save_cookie_settings')
```


Called from
: [`hideGlobalCookies()` in `./Sources/ManageServer.php`](../docs/manageserver.html#hideglobalcookies)

Notes
: Since 2.1

### integrate_general_security_settings

```php
call_integration_hook('integrate_general_security_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyGeneralSecuritySettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsecuritysettings)

Notes
: Since 2.1

### integrate_save_general_security_settings

```php
call_integration_hook('integrate_save_general_security_settings')
```


Called from
: [`ModifyGeneralSecuritySettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifygeneralsecuritysettings)

Notes
: Since 2.1

### integrate_modify_cache_settings

```php
call_integration_hook('integrate_modify_cache_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyCacheSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifycachesettings)

Notes
: Since 2.1

### integrate_save_cache_settings

```php
call_integration_hook('integrate_save_cache_settings')
```


Called from
: [`ModifyCacheSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifycachesettings)

Notes
: Since 2.1

### integrate_export_settings

```php
call_integration_hook('integrate_export_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyExportSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyexportsettings)

Notes
: Since 2.1

### integrate_save_export_settings

```php
call_integration_hook('integrate_save_export_settings')
```


Called from
: [`ModifyExportSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyexportsettings)

Notes
: Since 2.1

### integrate_loadavg_settings

```php
call_integration_hook('integrate_loadavg_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyLoadBalancingSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyloadbalancingsettings)

Notes
: Since 2.1

### integrate_save_loadavg_settings

```php
call_integration_hook('integrate_save_loadavg_settings')
```


Called from
: [`ModifyLoadBalancingSettings()` in `./Sources/ManageServer.php`](../docs/manageserver.html#modifyloadbalancingsettings)

Notes
: Since 2.1

### integrate_prepare_db_settings

```php
call_integration_hook('integrate_prepare_db_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`prepareDBSettingContext()` in `./Sources/ManageServer.php`](../docs/manageserver.html#preparedbsettingcontext)

Notes
: Since 2.1

### integrate_load_cache_apis

```php
call_integration_hook('integrate_load_cache_apis', array(&$loadedApis))
```

Type|Parameter|Description
---|---|---
`array`|`&$loadedApis`|desc

Called from
: [`loadCacheAPIs()` in `./Sources/ManageServer.php`](../docs/manageserver.html#loadcacheapis)

Notes
: Since 2.1


## ManageSettings.php
### integrate_modify_features

```php
call_integration_hook('integrate_modify_features', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ModifyFeatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifyfeaturesettings)

Notes
: Since 2.1

### integrate_modify_modifications

```php
call_integration_hook('integrate_modify_modifications', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ModifyModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymodsettings)

Notes
: Since 2.1

### integrate_modify_basic_settings

```php
call_integration_hook('integrate_modify_basic_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyBasicSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybasicsettings)

Notes
: Since 2.1

### integrate_save_basic_settings

```php
call_integration_hook('integrate_save_basic_settings')
```


Called from
: [`ModifyBasicSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybasicsettings)

Notes
: Since 2.1

### integrate_modify_bbc_settings

```php
call_integration_hook('integrate_modify_bbc_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyBBCSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybbcsettings)

Notes
: Since 2.1

### integrate_save_bbc_settings

```php
call_integration_hook('integrate_save_bbc_settings', array($bbcTags))
```

Type|Parameter|Description
---|---|---
`array`|`$bbcTags`|desc

Called from
: [`ModifyBBCSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifybbcsettings)

Notes
: Since 2.1

### integrate_layout_settings

```php
call_integration_hook('integrate_layout_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyLayoutSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylayoutsettings)

Notes
: Since 2.1

### integrate_save_layout_settings

```php
call_integration_hook('integrate_save_layout_settings')
```


Called from
: [`ModifyLayoutSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylayoutsettings)

Notes
: Since 2.1

### integrate_likes_settings

```php
call_integration_hook('integrate_likes_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyLikesSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylikessettings)

Notes
: Since 2.1

### integrate_save_likes_settings

```php
call_integration_hook('integrate_save_likes_settings')
```


Called from
: [`ModifyLikesSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylikessettings)

Notes
: Since 2.1

### integrate_mentions_settings

```php
call_integration_hook('integrate_mentions_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyMentionsSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymentionssettings)

Notes
: Since 2.1

### integrate_save_mentions_settings

```php
call_integration_hook('integrate_save_mentions_settings')
```


Called from
: [`ModifyMentionsSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifymentionssettings)

Notes
: Since 2.1

### integrate_warning_settings

```php
call_integration_hook('integrate_warning_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyWarningSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifywarningsettings)

Notes
: Since 2.1

### integrate_save_warning_settings

```php
call_integration_hook('integrate_save_warning_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$save_vars`|desc

Called from
: [`ModifyWarningSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifywarningsettings)

Notes
: Since 2.1

### integrate_spam_settings

```php
call_integration_hook('integrate_spam_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyAntispamSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifyantispamsettings)

Notes
: Since 2.1

### integrate_save_spam_settings

```php
call_integration_hook('integrate_save_spam_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$save_vars`|desc

Called from
: [`ModifyAntispamSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifyantispamsettings)

Notes
: Since 2.1

### integrate_signature_settings

```php
call_integration_hook('integrate_signature_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifySignatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifysignaturesettings)

Notes
: Since 2.1

### integrate_apply_signature_settings

```php
call_integration_hook('integrate_apply_signature_settings', array(&$sig, $sig_limits, $disabledTags))
```

Type|Parameter|Description
---|---|---
`array`|`&$sig`|desc
`array`|`$sig_limits`|desc
`array`|`$disabledTags`|desc

Called from
: [`ModifySignatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifysignaturesettings)

Notes
: Since 2.1

### integrate_save_signature_settings

```php
call_integration_hook('integrate_save_signature_settings', array(&$sig_limits, &$bbcTags))
```

Type|Parameter|Description
---|---|---
`array`|`&$sig_limits`|desc
`array`|`&$bbcTags`|desc

Called from
: [`ModifySignatureSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifysignaturesettings)

Notes
: Since 2.1

### integrate_prune_settings

```php
call_integration_hook('integrate_prune_settings', array(&$config_vars, &$prune_toggle, false))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc
`array`|`&$prune_toggle`|desc
`array`|`false`|desc

Called from
: [`ModifyLogSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifylogsettings)

Notes
: Since 2.1

### integrate_prune_settings

```php
call_integration_hook('integrate_prune_settings', array(&$savevar, &$prune_toggle, true))
```

Type|Parameter|Description
---|---|---
`array`|`&$savevar`|desc
`array`|`&$prune_toggle`|desc
`array`|`true`|desc

Called from
: [`togglePruned()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#togglepruned)

Notes
: Since 2.1

### integrate_general_mod_settings

```php
call_integration_hook('integrate_general_mod_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`ModifyGeneralModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifygeneralmodsettings)

Notes
: Since 2.1

### integrate_save_general_mod_settings

```php
call_integration_hook('integrate_save_general_mod_settings', array(&$save_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$save_vars`|desc

Called from
: [`ModifyGeneralModSettings()` in `./Sources/ManageSettings.php`](../docs/managesettings.html#modifygeneralmodsettings)

Notes
: Since 2.1


## ManageSmileys.php
### integrate_manage_smileys

```php
call_integration_hook('integrate_manage_smileys', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$subActions`|desc

Called from
: [`ManageSmileys()` in `./Sources/ManageSmileys.php`](../docs/managesmileys.html#managesmileys)

Notes
: Since 2.1

### integrate_modify_smiley_settings

```php
call_integration_hook('integrate_modify_smiley_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`&$config_vars`|desc

Called from
: [`EditSmileySettings()` in `./Sources/ManageSmileys.php`](../docs/managesmileys.html#editsmileysettings)

Notes
: Since 2.1

### integrate_save_smiley_settings

```php
call_integration_hook('integrate_save_smiley_settings')
```


Called from
: [`EditSmileySettings()` in `./Sources/ManageSmileys.php`](../docs/managesmileys.html#editsmileysettings)

Notes
: Since 2.1


## Subs-Admin.php
### integrate_update_settings_file

```php
call_integration_hook('integrate_update_settings_file', array(&$settings_defs))
```

Type|Parameter|Description
---|---|---
`array`|`&$settings_defs`|desc

Called from
: [`get_settings_defs()` in `./Sources/Subs-Admin.php`](../docs/subs-admin.html#get_settings_defs)

Notes
: Since 2.1

