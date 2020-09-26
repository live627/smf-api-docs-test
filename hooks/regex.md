---
layout: default
group: hooks
title: Regular expression to filter calls
---
* auto-gen TOC:
{:toc}
<https://regex101.com/r/qMjHcm/4>

```php
$re = '/.+(call_integration_hook\(\'(?P<hook>[\w]+)\'[, array\(]*(?P<param>|[^\)]+)\)).+/';
$str = './index.php:137:	call_integration_hook(\'integrate_autoload\', array(&$classMap));
./index.php:244:	call_integration_hook(\'integrate_pre_log_stats\', array(&$no_stat_actions));
./index.php:403:	call_integration_hook(\'integrate_actions\', array(&$actionArray));
./Sources/Admin.php:732:	call_integration_hook(\'integrate_admin_search\', array(&$language_files, &$include_files, &$settings_search));
./Sources/Admin.php:945:	call_integration_hook(\'integrate_manage_logs\', array(&$log_functions));
./Sources/Attachments.php:387:		call_integration_hook(\'integrate_attachment_upload\', array());
./Sources/BoardIndex.php:137:	call_integration_hook(\'integrate_mark_read_button\');
./Sources/Calendar.php:257:	call_integration_hook(\'integrate_calendar_buttons\');
./Sources/Display.php:151:	call_integration_hook(\'integrate_display_topic\', array(&$topic_selects, &$topic_tables, &$topic_parameters));
./Sources/Display.php:860:		call_integration_hook(\'integrate_poll_buttons\');
./Sources/Display.php:1032:	call_integration_hook(\'integrate_display_message_list\', array(&$messages, &$posters));
./Sources/Display.php:1202:		call_integration_hook(\'integrate_query_message\', array(&$msg_selects, &$msg_tables, &$msg_parameters));
./Sources/Display.php:1461:	call_integration_hook(\'integrate_display_buttons\', array(&$context[\'normal_buttons\']));
./Sources/Display.php:1463:	call_integration_hook(\'integrate_mod_buttons\', array(&$context[\'mod_buttons\']));
./Sources/Display.php:1753:	call_integration_hook(\'integrate_prepare_display_context\', array(&$output, &$message, $counter));
./Sources/Errors.php:114:		call_integration_hook(\'integrate_error_types\', array(&$other_error_types, &$error_type, $error_message, $file, $line));
./Sources/Errors.php:298:	call_integration_hook(\'integrate_output_error\', array($message, $error_type, $error_level, $file, $line));
./Sources/Groups.php:62:	call_integration_hook(\'integrate_manage_groups\', array(&$subActions));
./Sources/Help.php:36:	call_integration_hook(\'integrate_manage_help\', array(&$subActions));
./Sources/Help.php:110:	call_integration_hook(\'integrate_helpadmin\');
./Sources/Likes.php:233:			$can_like = call_integration_hook(\'integrate_valid_likes\', array($this->_type, $this->_content, $this->_sa, $this->_js, $this->_extra));
./Sources/Likes.php:306:		call_integration_hook(\'integrate_issue_like_before\', array(&$type, &$content, &$user, &$time));
./Sources/Likes.php:416:		call_integration_hook(\'integrate_issue_like\', array($this));
./Sources/Likes.php:616:		call_integration_hook(\'integrate_likes_json_response\', array(&$print));
./Sources/Load.php:314:			call_integration_hook(\'integrate_load_average\', array($modSettings[\'load_average\']));
./Sources/Load.php:432:	call_integration_hook(\'integrate_pre_load\');
./Sources/Load.php:454:	if (count($integration_ids = call_integration_hook(\'integrate_verify_user\')) > 0)
./Sources/Load.php:555:			call_integration_hook(\'integrate_force_tfasetup\', array(&$force_tfasetup));
./Sources/Load.php:575:			$verified = call_integration_hook(\'integrate_verify_tfa\', array($id_member, $user_settings));
./Sources/Load.php:850:	call_integration_hook(\'integrate_user_info\');
./Sources/Load.php:888:	call_integration_hook(\'integrate_load_min_user_settings_columns\', array(&$columns_to_load));
./Sources/Load.php:939:	call_integration_hook(\'integrate_load_min_user_settings\', array(&$user_info_min));
./Sources/Load.php:1037:		call_integration_hook(\'integrate_load_board\', array(&$custom_column_selects, &$custom_column_parameters));
./Sources/Load.php:1100:			call_integration_hook(\'integrate_board_info\', array(&$board_info, $row));
./Sources/Load.php:1458:	call_integration_hook(\'integrate_load_member_data\', array(&$select_columns, &$select_tables, &$set));
./Sources/Load.php:1803:	call_integration_hook(\'integrate_member_context\', array(&$memberContext[$user], $user, $display_custom_fields));
./Sources/Load.php:1978:	call_integration_hook(\'integrate_pre_load_theme\', array(&$id_theme));
./Sources/Load.php:2328:	call_integration_hook(\'integrate_simple_actions\', array(&$simpleActions, &$simpleAreas, &$simpleSubActions, &$extraParams, &$xmlActions));
./Sources/Load.php:2565:	call_integration_hook(\'integrate_load_theme\');
./Sources/Load.php:3609:	if (function_exists(\'call_integration_hook\'))
./Sources/Load.php:3610:		call_integration_hook(\'pre_cache_quick_get\', array(&$key, &$file, &$function, &$params, &$level));
./Sources/Load.php:3632:	if (function_exists(\'call_integration_hook\'))
./Sources/Load.php:3633:		call_integration_hook(\'post_cache_quick_get\', array(&$cache_block));
./Sources/Load.php:3674:	if (function_exists(\'call_integration_hook\'))
./Sources/Load.php:3675:		call_integration_hook(\'cache_put_data\', array(&$key, &$value, &$ttl));
./Sources/Load.php:3724:	if (function_exists(\'call_integration_hook\') && isset($value))
./Sources/Load.php:3725:		call_integration_hook(\'cache_get_data\', array(&$key, &$ttl, &$value));
./Sources/Load.php:3753:	call_integration_hook(\'integrate_clean_cache\');
./Sources/Load.php:3819:	call_integration_hook(\'integrate_set_avatar_data\', array(&$image, &$data));
./Sources/Logging.php:441:	call_integration_hook(\'integrate_log_types\', array(&$log_types, &$always_log));
./Sources/LogInOut.php:238:	if (in_array(\'retry\', call_integration_hook(\'integrate_validate_login\', array($_POST[\'user\'], isset($_POST[\'passwrd\']) ? $_POST[\'passwrd\'] : null, $modSettings[\'cookieTime\'])), true))
./Sources/LogInOut.php:361:		call_integration_hook(\'integrate_other_passwords\', array(&$other_passwords));
./Sources/LogInOut.php:562:	call_integration_hook(\'integrate_login\', array($user_settings[\'member_name\'], null, $modSettings[\'cookieTime\']));
./Sources/LogInOut.php:667:		call_integration_hook(\'integrate_logout\', array($user_settings[\'member_name\']));
./Sources/ManageAttachments.php:64:	call_integration_hook(\'integrate_manage_attachments\', array(&$subActions));
./Sources/ManageAttachments.php:188:	call_integration_hook(\'integrate_modify_attachment_settings\', array(&$config_vars));
./Sources/ManageAttachments.php:242:		call_integration_hook(\'integrate_save_attachment_settings\');
./Sources/ManageAttachments.php:340:	call_integration_hook(\'integrate_modify_avatar_settings\', array(&$config_vars));
./Sources/ManageAttachments.php:366:		call_integration_hook(\'integrate_save_avatar_settings\');
./Sources/ManageAttachments.php:591:	call_integration_hook(\'integrate_attachments_browse\', array(&$listOptions, &$titles, &$list_title));
./Sources/ManageAttachments.php:894:		call_integration_hook(\'integrate_attachment_remove\', array(&$filesRemoved, $attachments));
./Sources/ManageAttachments.php:1114:	call_integration_hook(\'integrate_remove_attachments\', array($attach));
./Sources/ManageAttachments.php:1534:			call_integration_hook(\'integrate_repair_attachments_nomsg\', array(&$ignore_ids, $_GET[\'substep\'], $_GET[\'substep\'] + 500));
./Sources/ManageAttachments.php:1902:	call_integration_hook(\'integrate_approve_attachments\', array($attachments));
./Sources/ManageBans.php:84:	call_integration_hook(\'integrate_manage_bans\', array(&$subActions));
./Sources/ManageBans.php:518:			call_integration_hook(\'integrate_ban_edit_list\', array(&$listOptions));
./Sources/ManageBans.php:613:			call_integration_hook(\'integrate_ban_edit_new\', array());
./Sources/ManageBans.php:723:	call_integration_hook(\'integrate_ban_list\', array(&$ban_items));
./Sources/ManageBans.php:767:	call_integration_hook(\'integrate_load_addtional_ip_ban\', array(&$search_list));
./Sources/ManageBans.php:871:		call_integration_hook(\'integrate_edit_bans\', array(&$ban_info, empty($_REQUEST[\'bg\'])));
./Sources/ManageBans.php:915:	call_integration_hook(\'integrate_edit_bans_post\', array());
./Sources/ManageBans.php:959:	call_integration_hook(\'integrate_save_triggers\', array(&$ban_triggers, &$ban_group));
./Sources/ManageBans.php:999:	call_integration_hook(\'integrate_remove_triggers\', array(&$items_ids, $group_id));
./Sources/ManageBoards.php:63:	call_integration_hook(\'integrate_manage_boards\', array(&$subActions));
./Sources/ManageBoards.php:203:	call_integration_hook(\'integrate_boards_main\');
./Sources/ManageBoards.php:302:	call_integration_hook(\'integrate_edit_category\');
./Sources/ManageBoards.php:609:	call_integration_hook(\'integrate_edit_board\');
./Sources/ManageBoards.php:863:	call_integration_hook(\'integrate_modify_board_settings\', array(&$config_vars));
./Sources/ManageBoards.php:890:		call_integration_hook(\'integrate_save_board_settings\');
./Sources/ManageCalendar.php:70:	call_integration_hook(\'integrate_manage_calendar\', array(&$subActions));
./Sources/ManageCalendar.php:378:	call_integration_hook(\'integrate_modify_calendar_settings\', array(&$config_vars));
./Sources/ManageCalendar.php:397:		call_integration_hook(\'integrate_save_calendar_settings\');
./Sources/ManageLanguages.php:56:	call_integration_hook(\'integrate_manage_languages\', array(&$subActions));
./Sources/ManageLanguages.php:753:	call_integration_hook(\'integrate_language_settings\', array(&$config_vars));
./Sources/ManageLanguages.php:768:		call_integration_hook(\'integrate_save_language_settings\', array(&$config_vars));
./Sources/ManageLanguages.php:866:	call_integration_hook(\'integrate_modifylanguages\', array(&$themes, &$lang_dirs, &$allows_add_remove, &$additional_string_types));
./Sources/ManageLanguages.php:1099:		call_integration_hook(\'integrate_language_edit_helptext\', array(&$special_groups));
./Sources/ManageMail.php:48:	call_integration_hook(\'integrate_manage_mail\', array(&$subActions));
./Sources/ManageMail.php:328:	call_integration_hook(\'integrate_modify_mail_settings\', array(&$config_vars));
./Sources/ManageMail.php:346:		call_integration_hook(\'integrate_save_mail_settings\');
./Sources/ManageMaintenance.php:95:	call_integration_hook(\'integrate_manage_maintenance\', array(&$subActions));
./Sources/ManageMaintenance.php:371:		call_integration_hook(\'integrate_convert_msgbody\', array($body_type));
./Sources/ManageMembergroups.php:63:	call_integration_hook(\'integrate_manage_membergroups\', array(&$subActions));
./Sources/ManageMembergroups.php:312:		call_integration_hook(\'integrate_pre_add_membergroup\', array());
./Sources/ManageMembergroups.php:328:		call_integration_hook(\'integrate_add_membergroup\', array($id_group, $postCountBasedGroup));
./Sources/ManageMembergroups.php:773:		call_integration_hook(\'integrate_save_membergroup\', array((int) $_REQUEST[\'group\']));
./Sources/ManageMembergroups.php:1217:	call_integration_hook(\'integrate_view_membergroup\');
./Sources/ManageMembergroups.php:1248:	call_integration_hook(\'integrate_modify_membergroup_settings\', array(&$config_vars));
./Sources/ManageMembergroups.php:1253:		call_integration_hook(\'integrate_save_membergroup_settings\');
./Sources/ManageMembers.php:100:	call_integration_hook(\'integrate_manage_members\', array(&$subActions));
./Sources/ManageMembers.php:260:		call_integration_hook(\'integrate_view_members_params\', array(&$params));
./Sources/ManageMembers.php:1122:				call_integration_hook(\'integrate_activate\', array($member[\'username\']));
./Sources/ManageNews.php:44:	call_integration_hook(\'integrate_manage_news\', array(&$subActions));
./Sources/ManageNews.php:1101:	call_integration_hook(\'integrate_modify_news_settings\', array(&$config_vars));
./Sources/ManageNews.php:1124:		call_integration_hook(\'integrate_save_news_settings\');
./Sources/ManagePaid.php:72:	call_integration_hook(\'integrate_manage_subscriptions\', array(&$subActions));
./Sources/ManagePaid.php:557:		call_integration_hook(\'integrate_delete_subscription\', array($context[\'sub_id\']));
./Sources/ManagePaid.php:689:		call_integration_hook(\'integrate_save_subscription\', array(($context[\'action_type\'] == \'add\' ? $id_subscribe : $context[\'sub_id\']), $_POST[\'name\'], $_POST[\'desc\'], $isActive, $span, $cost, $_POST[\'prim_group\'], $addgroups, $isRepeatable, $allowpartial, $emailComplete, $reminder));
./Sources/ManagePermissions.php:74:	call_integration_hook(\'integrate_manage_permissions\', array(&$subActions));
./Sources/ManagePermissions.php:1007:	call_integration_hook(\'integrate_modify_permission_settings\', array(&$config_vars));
./Sources/ManagePermissions.php:1024:		call_integration_hook(\'integrate_save_permission_settings\');
./Sources/ManagePermissions.php:1266:	call_integration_hook(\'integrate_load_permission_levels\', array(&$groupLevels, &$boardLevels));
./Sources/ManagePermissions.php:1633:	call_integration_hook(\'integrate_load_permissions\', array(&$permissionGroups, &$permissionList, &$leftPermissionGroups, &$hiddenPermissions, &$relabelPermissions));
./Sources/ManagePermissions.php:2289:	call_integration_hook(\'integrate_load_illegal_permissions\');
./Sources/ManagePermissions.php:2358:	call_integration_hook(\'integrate_load_illegal_guest_permissions\');
./Sources/ManagePermissions.php:2463:	call_integration_hook(\'integrate_post_moderation_mapping\', array(&$mappings));
./Sources/ManagePosts.php:68:	call_integration_hook(\'integrate_manage_posts\', array(&$subActions));
./Sources/ManagePosts.php:133:		call_integration_hook(\'integrate_save_censors\', array(&$updates));
./Sources/ManagePosts.php:164:	call_integration_hook(\'integrate_censors\');
./Sources/ManagePosts.php:230:	call_integration_hook(\'integrate_modify_post_settings\', array(&$config_vars));
./Sources/ManagePosts.php:265:		call_integration_hook(\'integrate_save_post_settings\');
./Sources/ManagePosts.php:326:	call_integration_hook(\'integrate_modify_topic_settings\', array(&$config_vars));
./Sources/ManagePosts.php:342:		call_integration_hook(\'integrate_save_topic_settings\');
./Sources/ManageRegistration.php:79:	call_integration_hook(\'integrate_manage_registrations\', array(&$subActions));
./Sources/ManageRegistration.php:344:	call_integration_hook(\'integrate_modify_registration_settings\', array(&$config_vars));
./Sources/ManageRegistration.php:364:		call_integration_hook(\'integrate_save_registration_settings\');
./Sources/ManageScheduledTasks.php:67:	call_integration_hook(\'integrate_manage_scheduled_tasks\', array(&$subActions));
./Sources/ManageScheduledTasks.php:657:	call_integration_hook(\'integrate_scheduled_tasks_settings\', array(&$config_vars));
./Sources/ManageScheduledTasks.php:676:		call_integration_hook(\'integrate_save_scheduled_tasks_settings\', array(&$save_vars));
./Sources/ManageSearch.php:74:	call_integration_hook(\'integrate_manage_search\', array(&$subActions));
./Sources/ManageSearch.php:106:	call_integration_hook(\'integrate_modify_search_settings\', array(&$config_vars));
./Sources/ManageSearch.php:128:		call_integration_hook(\'integrate_save_search_settings\');
./Sources/ManageSearch.php:170:	call_integration_hook(\'integrate_modify_search_weights\', array(&$factors));
./Sources/ManageSearch.php:178:		call_integration_hook(\'integrate_save_search_weights\');
./Sources/ManageSearchEngines.php:61:	call_integration_hook(\'integrate_manage_search_engines\', array(&$subActions));
./Sources/ManageSearchEngines.php:103:	call_integration_hook(\'integrate_modify_search_engine_settings\', array(&$config_vars));
./Sources/ManageSearchEngines.php:139:		call_integration_hook(\'integrate_save_search_engine_settings\');
./Sources/ManageServer.php:130:	call_integration_hook(\'integrate_server_settings\', array(&$subActions));
./Sources/ManageServer.php:184:	call_integration_hook(\'integrate_general_settings\', array(&$config_vars));
./Sources/ManageServer.php:196:		call_integration_hook(\'integrate_save_general_settings\');
./Sources/ManageServer.php:425:	call_integration_hook(\'integrate_database_settings\', array(&$config_vars));
./Sources/ManageServer.php:445:		call_integration_hook(\'integrate_save_database_settings\');
./Sources/ManageServer.php:519:	call_integration_hook(\'integrate_cookie_settings\', array(&$config_vars));
./Sources/ManageServer.php:530:		call_integration_hook(\'integrate_save_cookie_settings\');
./Sources/ManageServer.php:654:	call_integration_hook(\'integrate_general_security_settings\', array(&$config_vars));
./Sources/ManageServer.php:665:		call_integration_hook(\'integrate_save_general_security_settings\');
./Sources/ManageServer.php:719:	call_integration_hook(\'integrate_modify_cache_settings\', array(&$config_vars));
./Sources/ManageServer.php:742:		call_integration_hook(\'integrate_save_cache_settings\');
./Sources/ManageServer.php:803:	call_integration_hook(\'integrate_export_settings\', array(&$config_vars));
./Sources/ManageServer.php:840:		call_integration_hook(\'integrate_save_export_settings\');
./Sources/ManageServer.php:920:	call_integration_hook(\'integrate_loadavg_settings\', array(&$config_vars));
./Sources/ManageServer.php:947:		call_integration_hook(\'integrate_save_loadavg_settings\');
./Sources/ManageServer.php:1308:	call_integration_hook(\'integrate_prepare_db_settings\', array(&$config_vars));
./Sources/ManageSettings.php:100:	call_integration_hook(\'integrate_modify_features\', array(&$subActions));
./Sources/ManageSettings.php:137:	call_integration_hook(\'integrate_modify_modifications\', array(&$subActions));
./Sources/ManageSettings.php:257:	call_integration_hook(\'integrate_modify_basic_settings\', array(&$config_vars));
./Sources/ManageSettings.php:271:		call_integration_hook(\'integrate_save_basic_settings\');
./Sources/ManageSettings.php:328:	call_integration_hook(\'integrate_modify_bbc_settings\', array(&$config_vars));
./Sources/ManageSettings.php:383:		call_integration_hook(\'integrate_save_bbc_settings\', array($bbcTags));
./Sources/ManageSettings.php:428:	call_integration_hook(\'integrate_layout_settings\', array(&$config_vars));
./Sources/ManageSettings.php:438:		call_integration_hook(\'integrate_save_layout_settings\');
./Sources/ManageSettings.php:469:	call_integration_hook(\'integrate_likes_settings\', array(&$config_vars));
./Sources/ManageSettings.php:479:		call_integration_hook(\'integrate_save_likes_settings\');
./Sources/ManageSettings.php:508:	call_integration_hook(\'integrate_mentions_settings\', array(&$config_vars));
./Sources/ManageSettings.php:518:		call_integration_hook(\'integrate_save_mentions_settings\');
./Sources/ManageSettings.php:588:	call_integration_hook(\'integrate_warning_settings\', array(&$config_vars));
./Sources/ManageSettings.php:646:		call_integration_hook(\'integrate_save_warning_settings\', array(&$save_vars));
./Sources/ManageSettings.php:740:	call_integration_hook(\'integrate_spam_settings\', array(&$config_vars));
./Sources/ManageSettings.php:953:		call_integration_hook(\'integrate_save_spam_settings\', array(&$save_vars));
./Sources/ManageSettings.php:1043:	call_integration_hook(\'integrate_signature_settings\', array(&$config_vars));
./Sources/ManageSettings.php:1264:				call_integration_hook(\'integrate_apply_signature_settings\', array(&$sig, $sig_limits, $disabledTags));
./Sources/ManageSettings.php:1339:		call_integration_hook(\'integrate_save_signature_settings\', array(&$sig_limits, &$bbcTags));
./Sources/ManageSettings.php:2270:	call_integration_hook(\'integrate_prune_settings\', array(&$config_vars, &$prune_toggle, false));
./Sources/ManageSettings.php:2307:		call_integration_hook(\'integrate_prune_settings\', array(&$savevar, &$prune_toggle, true));
./Sources/ManageSettings.php:2357:	call_integration_hook(\'integrate_general_mod_settings\', array(&$config_vars));
./Sources/ManageSettings.php:2385:		call_integration_hook(\'integrate_save_general_mod_settings\', array(&$save_vars));
./Sources/ManageSmileys.php:103:	call_integration_hook(\'integrate_manage_smileys\', array(&$subActions));
./Sources/ManageSmileys.php:151:	call_integration_hook(\'integrate_modify_smiley_settings\', array(&$config_vars));
./Sources/ManageSmileys.php:171:		call_integration_hook(\'integrate_save_smiley_settings\');
./Sources/Memberlist.php:146:	call_integration_hook(\'integrate_memberlist_buttons\');
./Sources/Mentions.php:87:		call_integration_hook(\'mention_insert_\' . $content_type, array($content_id, &$members));
./Sources/MessageIndex.php:116:	call_integration_hook(\'integrate_pre_messageindex\', array(&$sort_methods, &$sort_methods_table));
./Sources/MessageIndex.php:318:	call_integration_hook(\'integrate_message_index\', array(&$message_index_selects, &$message_index_tables, &$message_index_parameters, &$message_index_wheres, &$topic_ids, &$message_index_topic_wheres));
./Sources/MessageIndex.php:607:		call_integration_hook(\'integrate_quick_mod_actions\');
./Sources/MessageIndex.php:738:	call_integration_hook(\'integrate_messageindex_buttons\', array(&$context[\'normal_buttons\']));
./Sources/ModerationCenter.php:278:	call_integration_hook(\'integrate_mod_centre_blocks\', array(&$valid_blocks));
./Sources/ModerationCenter.php:1392:	call_integration_hook(\'integrate_warning_log_actions\', array(&$subActions));
./Sources/Modlog.php:300:	call_integration_hook(\'integrate_viewModLog\', array(&$listOptions, &$moderation_menu_name));
./Sources/MoveTopic.php:359:	call_integration_hook(\'integrate_movetopic2_end\');
./Sources/News.php:58:	call_integration_hook(\'integrate_xmlfeeds\', array(&$subActions));
./Sources/News.php:349:	call_integration_hook(\'integrate_xml_data\', array(&$xml_data, &$feed_meta, &$namespaces, &$extraFeedTags, &$forceCdataKeys, &$nsKeys, $xml_format, $subaction, &$doctype));
./Sources/News.php:524:	call_integration_hook(\'integrate_fix_url\', array(&$val));
./Sources/PackageGet.php:77:	call_integration_hook(\'integrate_package_get\', array(&$subActions));
./Sources/PackageGet.php:639:	call_integration_hook(\'integrate_package_download\');
./Sources/PackageGet.php:729:	call_integration_hook(\'integrate_package_upload\');
./Sources/Packages.php:88:	call_integration_hook(\'integrate_manage_packages\', array(&$subActions));
./Sources/Packages.php:1390:	call_integration_hook(\'integrate_modification_types\');
./Sources/Packages.php:1605:		call_integration_hook(\'integrate_packages_sort_id\', array(&$sort_id, &$packages));
./Sources/PersonalMessage.php:940:			call_integration_hook(\'integrate_conversation_buttons\');
./Sources/PersonalMessage.php:1101:	call_integration_hook(\'integrate_prepare_pm_context\', array(&$output, &$message, $counter));
./Sources/PersonalMessage.php:1793:	call_integration_hook(\'integrate_search_pm_context\');
./Sources/PersonalMessage.php:2088:	call_integration_hook(\'integrate_pm_post\');
./Sources/PersonalMessage.php:2288:	call_integration_hook(\'integrate_pm_error\');
./Sources/Poll.php:219:	call_integration_hook(\'integrate_poll_vote\', array(&$row[\'id_poll\'], &$pollOptions));
./Sources/Poll.php:888:	call_integration_hook(\'integrate_poll_add_edit\', array($bcinfo[\'id_poll\'], $isEdit));
./Sources/Poll.php:1002:	call_integration_hook(\'integrate_poll_remove\', array($pollID));
./Sources/Post.php:49:	call_integration_hook(\'integrate_post_start\');
./Sources/Post.php:556:			call_integration_hook(\'integrate_preview_post\', array(&$form_message, &$form_subject));
./Sources/Post.php:1067:	call_integration_hook(\'integrate_post_errors\', array(&$post_errors, &$minor_errors, $form_message, $form_subject));
./Sources/Post.php:1532:	call_integration_hook(\'integrate_post_end\');
./Sources/Post.php:1587:	call_integration_hook(\'integrate_post2_start\', array(&$post_errors));
./Sources/Post.php:2048: 	call_integration_hook(\'integrate_post2_pre\', array(&$post_errors));
./Sources/Post.php:2242:		call_integration_hook(\'integrate_poll_add_edit\', array($id_poll, false));
./Sources/Post.php:2464:	call_integration_hook(\'integrate_post2_end\');
./Sources/Post.php:2789:	 	call_integration_hook(\'integrate_getTopic_previous_post\', array(&$row));
./Sources/Post.php:3026: 	call_integration_hook(\'integrate_post_JavascriptModify\', array(&$post_errors, $row));
./Sources/Post.php:3197:		call_integration_hook(\'integrate_jsmodify_xml\');
./Sources/PostModeration.php:45:	call_integration_hook(\'integrate_post_moderation\', array(&$subActions));
./Sources/Profile-Actions.php:41:		call_integration_hook(\'integrate_activate\', array($user_profile[$memID][\'member_name\']));
./Sources/Profile-Export.php:875:		call_integration_hook(\'integrate_export_xslt_variables\', array(&$xslt_variables, $format));
./Sources/Profile-Export.php:1760:	call_integration_hook(\'integrate_export_xslt_stylesheet\', array(&$stylesheet, $format));
./Sources/Profile-Export.php:1823:	call_integration_hook(\'integrate_pre_css_output\');
./Sources/Profile-Export.php:1861:	call_integration_hook(\'integrate_pre_javascript_output\', array(false));
./Sources/Profile-Export.php:1862:	call_integration_hook(\'integrate_pre_javascript_output\', array(true));
./Sources/Profile-Modify.php:299:						call_integration_hook(\'integrate_reset_pass\', array($cur_profile[\'member_name\'], $value, $_POST[\'passwrd1\']));
./Sources/Profile-Modify.php:659:	call_integration_hook(\'integrate_load_profile_fields\', array(&$profile_fields));
./Sources/Profile-Modify.php:694:	call_integration_hook(\'integrate_setup_profile_context\', array(&$fields));
./Sources/Profile-Modify.php:1335:	$hook_errors = call_integration_hook(\'integrate_save_custom_profile_fields\', array(&$changes, &$log_changes, &$errors, $returnErrors, $memID, $area, $sanitize, &$deletes));
./Sources/Profile-Modify.php:1436:		call_integration_hook(\'integrate_remove_buddy\', array($memID));
./Sources/Profile-Modify.php:1472:		call_integration_hook(\'integrate_add_buddies\', array($memID, &$new_buddies));
./Sources/Profile-Modify.php:1613:	call_integration_hook(\'integrate_view_buddies\', array($memID));
./Sources/Profile-Modify.php:1902:	call_integration_hook(\'integrate_theme_options\');
./Sources/Profile-Modify.php:2083:	call_integration_hook(\'integrate_alert_types\', array(&$alert_types, &$group_options));
./Sources/Profile-Modify.php:3356:	call_integration_hook(\'integrate_profile_profileSaveGroups\', array($value, $additional_groups));
./Sources/Profile-Modify.php:3381:	call_integration_hook(\'before_profile_save_avatar\', array(&$value));
./Sources/Profile-Modify.php:3643:	call_integration_hook(\'after_profile_save_avatar\');
./Sources/Profile-View.php:359:	call_integration_hook(\'integrate_fetch_alerts\', array(&$alerts, &$formats));
./Sources/Profile-View.php:1156:	call_integration_hook(\'integrate_profile_showPosts\');
./Sources/Profile-View.php:1830:	call_integration_hook(\'integrate_profile_stats\', array($memID, &$context[\'text_stats\']));
./Sources/Profile-View.php:2504:	call_integration_hook(\'integrate_profile_trackip\', array($ip_string, $ip_var));
./Sources/Profile.php:493:	call_integration_hook(\'integrate_pre_profile_areas\', array(&$profile_areas));
./Sources/Profile.php:680:			$good_password = in_array(true, call_integration_hook(\'integrate_verify_password\', array($cur_profile[\'member_name\'], $password, false)), true);
./Sources/Profile.php:734:		call_integration_hook(\'integrate_profile_save\', array(&$profile_vars, &$post_errors, $memID, $cur_profile, $current_area));
./Sources/Profile.php:747:				call_integration_hook(\'integrate_reset_pass\', array($cur_profile[\'member_name\'], $cur_profile[\'member_name\'], $_POST[\'passwrd2\']));
./Sources/Profile.php:890:	call_integration_hook(\'integrate_profile_popup\', array(&$profile_items));
./Sources/Profile.php:1085:	call_integration_hook(\'integrate_load_custom_profile_fields\', array($memID, $area));
./Sources/Recent.php:492:	call_integration_hook(\'integrate_recent_RecentPosts\');
./Sources/Recent.php:1465:	call_integration_hook(\'integrate_recent_buttons\');
./Sources/Recent.php:1470:	call_integration_hook(\'integrate_unread_list\');
./Sources/Register.php:583:		call_integration_hook(\'integrate_activate\', array($regOptions[\'username\']));
./Sources/Register.php:725:	call_integration_hook(\'integrate_activate\', array($row[\'member_name\']));
./Sources/Reminder.php:270:	call_integration_hook(\'integrate_reset_pass\', array($username, $username, $_POST[\'passwrd1\']));
./Sources/Reminder.php:397:	call_integration_hook(\'integrate_reset_pass\', array($row[\'member_name\'], $row[\'member_name\'], $_POST[\'passwrd1\']));
./Sources/RemoveTopic.php:259:	call_integration_hook(\'integrate_remove_topics_before\', array($topics, $recycle_board));
./Sources/RemoveTopic.php:564:	call_integration_hook(\'integrate_remove_topics\', array($topics));
./Sources/RemoveTopic.php:993:	call_integration_hook(\'integrate_remove_message\', array($message, $row, $recycle));
./Sources/ReportedContent.php:70:	call_integration_hook(\'integrate_reported_\' . $context[\'report_type\'], array(&$subActions));
./Sources/Reports.php:63:	call_integration_hook(\'integrate_report_types\');
./Sources/Reports.php:119:	call_integration_hook(\'integrate_report_buttons\');
./Sources/Reports.php:394:	call_integration_hook(\'integrate_reports_boardperm\', array(&$disabled_permissions));
./Sources/Reports.php:691:	call_integration_hook(\'integrate_reports_groupperm\', array(&$disabled_permissions));
./Sources/ScheduledTasks.php:282:	call_integration_hook(\'integrate_daily_maintenance\');
./Sources/ScheduledTasks.php:451:		call_integration_hook(\'integrate_daily_digest_lang\', array(&$langtxt, $lang));
./Sources/ScheduledTasks.php:541:		call_integration_hook(\'integrate_daily_digest_email\', array(&$email, $types, $notify_types, $langtxt));
./Sources/ScheduledTasks.php:1322:	call_integration_hook(\'integrate_weekly_maintenance\');
./Sources/Search.php:230:	call_integration_hook(\'integrate_search\');
./Sources/Search.php:290:	call_integration_hook(\'integrate_search_weights\', array(&$weight_factors));
./Sources/Search.php:618:	call_integration_hook(\'integrate_search_sort_columns\', array(&$sort_columns));
./Sources/Search.php:641:	call_integration_hook(\'integrate_search_params\', array(&$search_params));
./Sources/Search.php:651:	call_integration_hook(\'integrate_search_blacklisted_words\', array(&$blacklisted_words));
./Sources/Search.php:1016:	call_integration_hook(\'integrate_search_errors\');
./Sources/Search.php:1178:					call_integration_hook(\'integrate_subject_only_search_query\', array(&$subject_query, &$subject_query_params));
./Sources/Search.php:1428:						call_integration_hook(\'integrate_subject_search_query\', array(&$subject_query));
./Sources/Search.php:1644:				call_integration_hook(\'integrate_main_search_query\', array(&$main_query));
./Sources/Search.php:1886:		call_integration_hook(\'integrate_search_message_list\', array(&$msg_list, &$posters));
./Sources/Search.php:2222:		call_integration_hook(\'integrate_quick_mod_actions_search\');
./Sources/Search.php:2247:	call_integration_hook(\'integrate_search_message_context\', array(&$output, &$message, $counter));
./Sources/Security.php:39:	call_integration_hook(\'integrate_validateSession\', array(&$types));
./Sources/Security.php:67:		$good_password = in_array(true, call_integration_hook(\'integrate_verify_password\', array($user_info[\'username\'], $_POST[$type . \'_pass\'], false)), true);
./Sources/Security.php:438:		call_integration_hook(\'integrate_post_ban_permissions\', array(&$denied_permissions));
./Sources/Security.php:451:		call_integration_hook(\'integrate_warn_permissions\', array(&$permission_change));
./Sources/Security.php:1008:	call_integration_hook(\'integrate_heavy_permissions_session\', array(&$heavy_permissions));
./Sources/Security.php:1166:	call_integration_hook(\'integrate_spam_protection\', array(&$timeOverrides));
./Sources/Session.php:38:	call_integration_hook(\'integrate_load_session\');
./Sources/Session.php:79:			call_integration_hook(\'integrate_session_handlers\');
./Sources/ShowAttachments.php:36:	call_integration_hook(\'integrate_pre_download_request\');
./Sources/ShowAttachments.php:87:		call_integration_hook(\'integrate_download_request\', array(&$attachRequest));
./Sources/SplitTopics.php:813:	call_integration_hook(\'integrate_split_topic\', array($split1, $split2, $new_subject, $id_board));
./Sources/SplitTopics.php:1764:	call_integration_hook(\'integrate_merge_topic\', array($merged_topic, $updated_topics, $deleted_topics, $deleted_polls));
./Sources/Stats.php:696:	call_integration_hook(\'integrate_forum_stats\');
./Sources/Subs-Admin.php:904:	if (function_exists(\'call_integration_hook\'))
./Sources/Subs-Admin.php:905:		call_integration_hook(\'integrate_update_settings_file\', array(&$settings_defs));
./Sources/Subs-Attachments.php:476:	call_integration_hook(\'integrate_attachment_upload\', array());
./Sources/Subs-Attachments.php:714:	call_integration_hook(\'integrate_createAttachment\', array(&$attachmentOptions, &$attachmentInserts));
./Sources/Subs-Attachments.php:903:	call_integration_hook(\'integrate_assign_attachments\', array(&$attachIDs, &$msgID));
./Sources/Subs-Attachments.php:946:	$externalParse = call_integration_hook(\'integrate_pre_parseAttachBBC\', array($attachID, $msgID));
./Sources/Subs-Attachments.php:1032:	call_integration_hook(\'integrate_post_parseAttachBBC\', array(&$attachContext));
./Sources/Subs-Auth.php:77:	call_integration_hook(\'integrate_cookie_data\', array($data, &$custom_data));
./Sources/Subs-Auth.php:267:	call_integration_hook(\'integrate_validateSession\', array(&$types));
./Sources/Subs-Auth.php:635:	call_integration_hook(\'integrate_reset_pass\', array($old_user, $user, $newPassword));
./Sources/Subs-Auth.php:830:	call_integration_hook(\'integrate_mod_cache\');
./Sources/Subs-Auth.php:860:	call_integration_hook(\'integrate_cookie\', array($name, $value, $expire, $path, $domain, $secure, $httponly));
./Sources/Subs-BoardIndex.php:70:	call_integration_hook(\'integrate_pre_boardindex\', array(&$board_index_selects, &$board_index_parameters));
./Sources/Subs-BoardIndex.php:237:				call_integration_hook(\'integrate_boardindex_board\', array(&$this_category, $row_board));
./Sources/Subs-BoardIndex.php:484:		call_integration_hook(\'integrate_getboardtree\', array($board_index_options, &$categories));
./Sources/Subs-BoardIndex.php:486:		call_integration_hook(\'integrate_getboardtree\', array($board_index_options, &$this_category));
./Sources/Subs-Boards.php:466:	call_integration_hook(\'integrate_pre_modify_board\', array($id, &$boardOptions));
./Sources/Subs-Boards.php:646:	call_integration_hook(\'integrate_modify_board\', array($id, $boardOptions, &$boardUpdates, &$boardUpdateParameters));
./Sources/Subs-Boards.php:888:	call_integration_hook(\'integrate_create_board\', array(&$boardOptions, &$board_columns, &$board_parameters));
./Sources/Subs-Boards.php:981:	call_integration_hook(\'integrate_delete_board\', array($boards_to_remove, &$moveChildrenTo));
./Sources/Subs-Boards.php:1389:	call_integration_hook(\'integrate_pre_boardtree\', array(&$boardColumns, &$boardParameters, &$boardJoins, &$boardWhere, &$boardOrder));
./Sources/Subs-Boards.php:1496:		call_integration_hook(\'integrate_boardtree_board\', array($row));
./Sources/Subs-Calendar.php:1197:	call_integration_hook(\'integrate_create_event\', array(&$eventOptions, &$event_columns, &$event_parameters));
./Sources/Subs-Calendar.php:1278:	call_integration_hook(\'integrate_modify_event\', array($event_id, &$eventOptions, &$event_columns, &$event_parameters));
./Sources/Subs-Calendar.php:1333:	call_integration_hook(\'integrate_remove_event\', array($event_id));
./Sources/Subs-Categories.php:35:	call_integration_hook(\'integrate_pre_modify_category\', array($cat_id, &$catOptions));
./Sources/Subs-Categories.php:104:	call_integration_hook(\'integrate_modify_category\', array($cat_id, &$catUpdates, &$catParameters));
./Sources/Subs-Categories.php:160:	call_integration_hook(\'integrate_create_category\', array(&$catOptions, &$cat_columns, &$cat_parameters));
./Sources/Subs-Categories.php:199:	call_integration_hook(\'integrate_delete_category\', array($categories, &$moveBoardsTo));
./Sources/Subs-Editor.php:1496:	call_integration_hook(\'integrate_load_message_icons\', array(&$icons));
./Sources/Subs-Editor.php:1767:		call_integration_hook(\'integrate_bbc_buttons\', array(&$context[\'bbc_tags\'], &$editor_tag_map));
./Sources/Subs-Editor.php:1974:	call_integration_hook(\'integrate_sceditor_options\', array(&$sce_options));
./Sources/Subs-Editor.php:2027:	call_integration_hook(\'integrate_create_control_verification_pre\', array(&$verificationOptions, $do_test));
./Sources/Subs-Editor.php:2161:		call_integration_hook(\'integrate_create_control_verification_test\', array($thisVerification, &$verification_errors));
./Sources/Subs-Editor.php:2236:		call_integration_hook(\'integrate_create_control_verification_refresh\', array($thisVerification));
./Sources/Subs-Editor.php:2275:	call_integration_hook(\'integrate_create_control_verification_post\', array(&$verification_errors, $do_test));
./Sources/Subs-Editor.php:2305:	call_integration_hook(\'integrate_autosuggest\', array(&$searchTypes));
./Sources/Subs-List.php:40:	call_integration_hook(\'integrate_\' . $listOptions[\'id\'], array(&$listOptions));
./Sources/Subs-Membergroups.php:109:	call_integration_hook(\'integrate_delete_membergroups\', array($groups));
./Sources/Subs-Membergroups.php:601:	call_integration_hook(\'integrate_add_members_to_group\', array($members, $group, &$group_names));
./Sources/Subs-Membergroups.php:682:	call_integration_hook(\'integrate_getMembergroupList\', array(&$groupCache, $group));
./Sources/Subs-Members.php:412:	call_integration_hook(\'integrate_delete_members\', array($users));
./Sources/Subs-Members.php:540:	call_integration_hook(\'integrate_register_check\', array(&$regOptions, &$reg_errors));
./Sources/Subs-Members.php:691:	call_integration_hook(\'integrate_register\', array(&$regOptions, &$theme_vars, &$knownInts, &$knownFloats));
./Sources/Subs-Members.php:721:	call_integration_hook(\'integrate_post_register\', array(&$regOptions, &$theme_vars, &$memberID));
./Sources/Subs-Members.php:846:	call_integration_hook(\'integrate_register_after\', array($regOptions, $memberID));
./Sources/Subs-Members.php:957:	call_integration_hook(\'integrate_check_name\', array($checkName, &$is_reserved, $current_id_member, $is_name));
./Sources/Subs-Members.php:1265:	call_integration_hook(\'integrate_reattribute_posts\', array($memID, $email, $membername, $post_count, &$updated));
./Sources/Subs-Menu.php:75:		call_integration_hook(\'integrate_\' . $menu_context[\'current_action\'] . \'_areas\', array(&$menuData));
./Sources/Subs-Post.php:262:	call_integration_hook(\'integrate_preparsecode\', array(&$message, $previewing));
./Sources/Subs-Post.php:275:	call_integration_hook(\'integrate_unpreparsecode\', array(&$message));
./Sources/Subs-Post.php:592:	if (in_array(false, call_integration_hook(\'integrate_outgoing_email\', array(&$subject, &$message, &$headers, &$to_array)), true))
./Sources/Subs-Post.php:856:	call_integration_hook(\'integrate_personal_message\', array(&$recipients, &$from, &$subject, &$message));
./Sources/Subs-Post.php:1197:	call_integration_hook(\'integrate_personal_message_after\', array(&$id_pm, &$log, &$recipients, &$from, &$subject, &$message));
./Sources/Subs-Post.php:1809:	call_integration_hook(\'integrate_create_post\', array(&$msgOptions, &$topicOptions, &$posterOptions, &$message_columns, &$message_parameters));
./Sources/Subs-Post.php:1837:	call_integration_hook(\'integrate_after_create_post\', array($msgOptions, $topicOptions, $posterOptions, $message_columns, $message_parameters));
./Sources/Subs-Post.php:1855:		call_integration_hook(\'integrate_before_create_topic\', array(&$msgOptions, &$topicOptions, &$posterOptions, &$topic_columns, &$topic_parameters));
./Sources/Subs-Post.php:1898:		call_integration_hook(\'integrate_create_topic\', array(&$msgOptions, &$topicOptions, &$posterOptions));
./Sources/Subs-Post.php:1926:		call_integration_hook(\'integrate_modify_topic\', array(&$topics_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions));
./Sources/Subs-Post.php:2210:	call_integration_hook(\'integrate_modify_post\', array(&$messages_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions, &$messageInts));
./Sources/Subs-Post.php:2559:	call_integration_hook(\'integrate_after_approve_posts\', array($approve, $msgs, $topic_changes, $member_post_changes));
./Sources/Subs-Themes.php:50:	call_integration_hook(\'integrate_get_single_theme\', array(&$themeValues, $id));
./Sources/Subs-Themes.php:124:	call_integration_hook(\'integrate_get_all_themes\', array(&$themeValues, $enable_only));
./Sources/Subs-Themes.php:193:	call_integration_hook(\'integrate_get_installed_themes\', array(&$themeValues));
./Sources/Subs-Themes.php:468:	call_integration_hook(\'integrate_theme_install\', array(&$context[\'to_install\'], $id_theme));
./Sources/Subs.php:344:					call_integration_hook(\'integrate_change_member_data\', array($member_names, $var, &$data[$var], &$knownInts, &$knownFloats));
./Sources/Subs.php:1246:	call_integration_hook(\'integrate_pre_parsebbc\', array(&$message, &$smileys, &$cache_id, &$parse_tags));
./Sources/Subs.php:1491:					call_integration_hook(\'integrate_attach_bbc_validate\', array(&$returnContext, $currentAttachment, $tag, $data, $disabled, $params));
./Sources/Subs.php:2132:		call_integration_hook(\'integrate_bbc_codes\', array(&$codes, &$no_autolink_tags));
./Sources/Subs.php:2250:		call_integration_hook(\'integrate_bbc_print\', array(&$disabled));
./Sources/Subs.php:3168:	call_integration_hook(\'integrate_post_parsebbc\', array(&$message, &$smileys, &$cache_id, &$parse_tags));
./Sources/Subs.php:3207:	call_integration_hook(\'integrate_smileys\', array(&$smileyPregSearch, &$smileyPregReplacements));
./Sources/Subs.php:3346:	call_integration_hook(\'integrate_proxy\', array($url, &$proxied_url));
./Sources/Subs.php:3397:	call_integration_hook(\'integrate_redirect\', array(&$setLocation, &$refresh, &$permanent));
./Sources/Subs.php:3504:	call_integration_hook(\'integrate_exit\', array($do_footer));
./Sources/Subs.php:3782:	call_integration_hook(\'integrate_theme_context\');
./Sources/Subs.php:3899:			call_integration_hook(\'integrate_security_files\', array(&$securityFiles));
./Sources/Subs.php:4021:	call_integration_hook(\'integrate_pre_javascript_output\', array(&$do_deferred));
./Sources/Subs.php:4154:	call_integration_hook(\'integrate_pre_css_output\');
./Sources/Subs.php:4867:		call_integration_hook(\'integrate_menu_buttons\', array(&$buttons));
./Sources/Subs.php:5016:		call_integration_hook(\'integrate_current_action\', array(&$current_action));
./Sources/Subs.php:5039:function call_integration_hook($hook, $parameters = array())
./Sources/tasks/Likes-Notify.php:64:			$hook_results = call_integration_hook(\'integrate_find_like_author\', array($this->_details[\'content_type\'], $this->_details[\'content_id\']));
./Sources/Themes.php:100:	call_integration_hook(\'integrate_manage_themes\', array(&$subActions));
./Sources/Themes.php:563:	call_integration_hook(\'integrate_theme_options\');
./Sources/Themes.php:694:	call_integration_hook(\'integrate_theme_settings\');
./Sources/Themes.php:1498:		call_integration_hook(\'integrate_wrap_action\');
./Sources/ViewQuery.php:50:	call_integration_hook(\'integrate_egg_nog\');
./Sources/Who.php:315:	call_integration_hook(\'who_allowed\', array(&$allowedActions));
./Sources/Who.php:465:		if (count($integrate_actions = call_integration_hook(\'integrate_whos_online\', array($actions))) > 0)
./Sources/Who.php:560:	call_integration_hook(\'whos_online_after\', array(&$urls, &$data));
./Sources/Who.php:893:	call_integration_hook(\'integrate_credits\');
./Sources/Xml.php:33:	call_integration_hook(\'integrate_XMLhttpMain_subActions\', array(&$subActions));
./SSI.php:132:	call_integration_hook(\'integrate_autoload\', array(&$classMap));
./SSI.php:234:call_integration_hook(\'integrate_SSI\');
./SSI.php:568:	call_integration_hook(\'integrate_ssi_queryPosts\', array(&$posts));
./SSI.php:737:	call_integration_hook(\'integrate_ssi_recentTopics\', array(&$posts));
./SSI.php:796:	call_integration_hook(\'integrate_ssi_topPoster\', array(&$return));
./SSI.php:851:	call_integration_hook(\'integrate_ssi_topBoards\', array(&$boards));
./SSI.php:946:	call_integration_hook(\'integrate_ssi_topTopics\', array(&$topics, $type));
./SSI.php:1153:	call_integration_hook(\'integrate_ssi_queryMembers\', array(&$members));
./SSI.php:1232:	call_integration_hook(\'integrate_ssi_boardStats\', array(&$totals));
./SSI.php:1262:	call_integration_hook(\'integrate_ssi_whosOnline\', array(&$return));
./SSI.php:1485:	call_integration_hook(\'integrate_ssi_recentPoll\', array(&$return, $topPollInstead));
./SSI.php:1654:	call_integration_hook(\'integrate_ssi_showPoll\', array(&$return));
./SSI.php:1856:	call_integration_hook(\'integrate_ssi_news\');
./SSI.php:1884:	call_integration_hook(\'integrate_ssi_calendar\', array(&$return, $eventOptions));
./SSI.php:1914:	call_integration_hook(\'integrate_ssi_calendar\', array(&$return, $eventOptions));
./SSI.php:1943:	call_integration_hook(\'integrate_ssi_calendar\', array(&$return, $eventOptions));
./SSI.php:1980:	call_integration_hook(\'integrate_ssi_calendar\', array(&$return, $eventOptions));
./SSI.php:2197:	call_integration_hook(\'integrate_ssi_boardNews\', array(&$return));
./SSI.php:2337:	call_integration_hook(\'integrate_ssi_recentEvents\', array(&$return));
./SSI.php:2486:	call_integration_hook(\'integrate_ssi_recentAttachments\', array(&$attachments));
./Themes/default/index.template.php:637:		call_integration_hook(\'integrate_\' . $list_class . \'_quickbuttons\', array(&$list_items));
./Themes/default/Post.template.php:472:		call_integration_hook(\'integrate_upload_template\');';
$subst = '### $2\\n\\n```php\\n$1\\n```\\nType|Parameter|Description\\n---|---|---\\n`var`|`$3`|desc\\n';

$result = preg_replace($re, $subst, $str);

echo "The result of the substitution is ".$result;
```

### Output
``````
### integrate_autoload

```php
call_integration_hook('integrate_autoload', array(&$classMap)
```
Type|Parameter|Description
---|---|---
`var`|`&$classMap`|desc

### integrate_pre_log_stats

```php
call_integration_hook('integrate_pre_log_stats', array(&$no_stat_actions)
```
Type|Parameter|Description
---|---|---
`var`|`&$no_stat_actions`|desc

### integrate_actions

```php
call_integration_hook('integrate_actions', array(&$actionArray)
```
Type|Parameter|Description
---|---|---
`var`|`&$actionArray`|desc

### integrate_admin_search

```php
call_integration_hook('integrate_admin_search', array(&$language_files, &$include_files, &$settings_search)
```
Type|Parameter|Description
---|---|---
`var`|`&$language_files, &$include_files, &$settings_search`|desc

### integrate_manage_logs

```php
call_integration_hook('integrate_manage_logs', array(&$log_functions)
```
Type|Parameter|Description
---|---|---
`var`|`&$log_functions`|desc

### integrate_attachment_upload

```php
call_integration_hook('integrate_attachment_upload', array()
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_mark_read_button

```php
call_integration_hook('integrate_mark_read_button')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_calendar_buttons

```php
call_integration_hook('integrate_calendar_buttons')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_display_topic

```php
call_integration_hook('integrate_display_topic', array(&$topic_selects, &$topic_tables, &$topic_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$topic_selects, &$topic_tables, &$topic_parameters`|desc

### integrate_poll_buttons

```php
call_integration_hook('integrate_poll_buttons')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_display_message_list

```php
call_integration_hook('integrate_display_message_list', array(&$messages, &$posters)
```
Type|Parameter|Description
---|---|---
`var`|`&$messages, &$posters`|desc

### integrate_query_message

```php
call_integration_hook('integrate_query_message', array(&$msg_selects, &$msg_tables, &$msg_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$msg_selects, &$msg_tables, &$msg_parameters`|desc

### integrate_display_buttons

```php
call_integration_hook('integrate_display_buttons', array(&$context['normal_buttons'])
```
Type|Parameter|Description
---|---|---
`var`|`&$context['normal_buttons']`|desc

### integrate_mod_buttons

```php
call_integration_hook('integrate_mod_buttons', array(&$context['mod_buttons'])
```
Type|Parameter|Description
---|---|---
`var`|`&$context['mod_buttons']`|desc

### integrate_prepare_display_context

```php
call_integration_hook('integrate_prepare_display_context', array(&$output, &$message, $counter)
```
Type|Parameter|Description
---|---|---
`var`|`&$output, &$message, $counter`|desc

### integrate_error_types

```php
call_integration_hook('integrate_error_types', array(&$other_error_types, &$error_type, $error_message, $file, $line)
```
Type|Parameter|Description
---|---|---
`var`|`&$other_error_types, &$error_type, $error_message, $file, $line`|desc

### integrate_output_error

```php
call_integration_hook('integrate_output_error', array($message, $error_type, $error_level, $file, $line)
```
Type|Parameter|Description
---|---|---
`var`|`$message, $error_type, $error_level, $file, $line`|desc

### integrate_manage_groups

```php
call_integration_hook('integrate_manage_groups', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_manage_help

```php
call_integration_hook('integrate_manage_help', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_helpadmin

```php
call_integration_hook('integrate_helpadmin')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_valid_likes

```php
call_integration_hook('integrate_valid_likes', array($this->_type, $this->_content, $this->_sa, $this->_js, $this->_extra)
```
Type|Parameter|Description
---|---|---
`var`|`$this->_type, $this->_content, $this->_sa, $this->_js, $this->_extra`|desc

### integrate_issue_like_before

```php
call_integration_hook('integrate_issue_like_before', array(&$type, &$content, &$user, &$time)
```
Type|Parameter|Description
---|---|---
`var`|`&$type, &$content, &$user, &$time`|desc

### integrate_issue_like

```php
call_integration_hook('integrate_issue_like', array($this)
```
Type|Parameter|Description
---|---|---
`var`|`$this`|desc

### integrate_likes_json_response

```php
call_integration_hook('integrate_likes_json_response', array(&$print)
```
Type|Parameter|Description
---|---|---
`var`|`&$print`|desc

### integrate_load_average

```php
call_integration_hook('integrate_load_average', array($modSettings['load_average'])
```
Type|Parameter|Description
---|---|---
`var`|`$modSettings['load_average']`|desc

### integrate_pre_load

```php
call_integration_hook('integrate_pre_load')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_verify_user

```php
call_integration_hook('integrate_verify_user')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_force_tfasetup

```php
call_integration_hook('integrate_force_tfasetup', array(&$force_tfasetup)
```
Type|Parameter|Description
---|---|---
`var`|`&$force_tfasetup`|desc

### integrate_verify_tfa

```php
call_integration_hook('integrate_verify_tfa', array($id_member, $user_settings)
```
Type|Parameter|Description
---|---|---
`var`|`$id_member, $user_settings`|desc

### integrate_user_info

```php
call_integration_hook('integrate_user_info')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_load_min_user_settings_columns

```php
call_integration_hook('integrate_load_min_user_settings_columns', array(&$columns_to_load)
```
Type|Parameter|Description
---|---|---
`var`|`&$columns_to_load`|desc

### integrate_load_min_user_settings

```php
call_integration_hook('integrate_load_min_user_settings', array(&$user_info_min)
```
Type|Parameter|Description
---|---|---
`var`|`&$user_info_min`|desc

### integrate_load_board

```php
call_integration_hook('integrate_load_board', array(&$custom_column_selects, &$custom_column_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$custom_column_selects, &$custom_column_parameters`|desc

### integrate_board_info

```php
call_integration_hook('integrate_board_info', array(&$board_info, $row)
```
Type|Parameter|Description
---|---|---
`var`|`&$board_info, $row`|desc

### integrate_load_member_data

```php
call_integration_hook('integrate_load_member_data', array(&$select_columns, &$select_tables, &$set)
```
Type|Parameter|Description
---|---|---
`var`|`&$select_columns, &$select_tables, &$set`|desc

### integrate_member_context

```php
call_integration_hook('integrate_member_context', array(&$memberContext[$user], $user, $display_custom_fields)
```
Type|Parameter|Description
---|---|---
`var`|`&$memberContext[$user], $user, $display_custom_fields`|desc

### integrate_pre_load_theme

```php
call_integration_hook('integrate_pre_load_theme', array(&$id_theme)
```
Type|Parameter|Description
---|---|---
`var`|`&$id_theme`|desc

### integrate_simple_actions

```php
call_integration_hook('integrate_simple_actions', array(&$simpleActions, &$simpleAreas, &$simpleSubActions, &$extraParams, &$xmlActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$simpleActions, &$simpleAreas, &$simpleSubActions, &$extraParams, &$xmlActions`|desc

### integrate_load_theme

```php
call_integration_hook('integrate_load_theme')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

./Sources/Load.php:3609:	if (function_exists('call_integration_hook'))
### pre_cache_quick_get

```php
call_integration_hook('pre_cache_quick_get', array(&$key, &$file, &$function, &$params, &$level)
```
Type|Parameter|Description
---|---|---
`var`|`&$key, &$file, &$function, &$params, &$level`|desc

./Sources/Load.php:3632:	if (function_exists('call_integration_hook'))
### post_cache_quick_get

```php
call_integration_hook('post_cache_quick_get', array(&$cache_block)
```
Type|Parameter|Description
---|---|---
`var`|`&$cache_block`|desc

./Sources/Load.php:3674:	if (function_exists('call_integration_hook'))
### cache_put_data

```php
call_integration_hook('cache_put_data', array(&$key, &$value, &$ttl)
```
Type|Parameter|Description
---|---|---
`var`|`&$key, &$value, &$ttl`|desc

./Sources/Load.php:3724:	if (function_exists('call_integration_hook') && isset($value))
### cache_get_data

```php
call_integration_hook('cache_get_data', array(&$key, &$ttl, &$value)
```
Type|Parameter|Description
---|---|---
`var`|`&$key, &$ttl, &$value`|desc

### integrate_clean_cache

```php
call_integration_hook('integrate_clean_cache')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_set_avatar_data

```php
call_integration_hook('integrate_set_avatar_data', array(&$image, &$data)
```
Type|Parameter|Description
---|---|---
`var`|`&$image, &$data`|desc

### integrate_log_types

```php
call_integration_hook('integrate_log_types', array(&$log_types, &$always_log)
```
Type|Parameter|Description
---|---|---
`var`|`&$log_types, &$always_log`|desc

### integrate_validate_login

```php
call_integration_hook('integrate_validate_login', array($_POST['user'], isset($_POST['passwrd'])
```
Type|Parameter|Description
---|---|---
`var`|`$_POST['user'], isset($_POST['passwrd']`|desc

### integrate_other_passwords

```php
call_integration_hook('integrate_other_passwords', array(&$other_passwords)
```
Type|Parameter|Description
---|---|---
`var`|`&$other_passwords`|desc

### integrate_login

```php
call_integration_hook('integrate_login', array($user_settings['member_name'], null, $modSettings['cookieTime'])
```
Type|Parameter|Description
---|---|---
`var`|`$user_settings['member_name'], null, $modSettings['cookieTime']`|desc

### integrate_logout

```php
call_integration_hook('integrate_logout', array($user_settings['member_name'])
```
Type|Parameter|Description
---|---|---
`var`|`$user_settings['member_name']`|desc

### integrate_manage_attachments

```php
call_integration_hook('integrate_manage_attachments', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_attachment_settings

```php
call_integration_hook('integrate_modify_attachment_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_attachment_settings

```php
call_integration_hook('integrate_save_attachment_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_avatar_settings

```php
call_integration_hook('integrate_modify_avatar_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_avatar_settings

```php
call_integration_hook('integrate_save_avatar_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_attachments_browse

```php
call_integration_hook('integrate_attachments_browse', array(&$listOptions, &$titles, &$list_title)
```
Type|Parameter|Description
---|---|---
`var`|`&$listOptions, &$titles, &$list_title`|desc

### integrate_attachment_remove

```php
call_integration_hook('integrate_attachment_remove', array(&$filesRemoved, $attachments)
```
Type|Parameter|Description
---|---|---
`var`|`&$filesRemoved, $attachments`|desc

### integrate_remove_attachments

```php
call_integration_hook('integrate_remove_attachments', array($attach)
```
Type|Parameter|Description
---|---|---
`var`|`$attach`|desc

### integrate_repair_attachments_nomsg

```php
call_integration_hook('integrate_repair_attachments_nomsg', array(&$ignore_ids, $_GET['substep'], $_GET['substep'] + 500)
```
Type|Parameter|Description
---|---|---
`var`|`&$ignore_ids, $_GET['substep'], $_GET['substep'] + 500`|desc

### integrate_approve_attachments

```php
call_integration_hook('integrate_approve_attachments', array($attachments)
```
Type|Parameter|Description
---|---|---
`var`|`$attachments`|desc

### integrate_manage_bans

```php
call_integration_hook('integrate_manage_bans', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_ban_edit_list

```php
call_integration_hook('integrate_ban_edit_list', array(&$listOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$listOptions`|desc

### integrate_ban_edit_new

```php
call_integration_hook('integrate_ban_edit_new', array()
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_ban_list

```php
call_integration_hook('integrate_ban_list', array(&$ban_items)
```
Type|Parameter|Description
---|---|---
`var`|`&$ban_items`|desc

### integrate_load_addtional_ip_ban

```php
call_integration_hook('integrate_load_addtional_ip_ban', array(&$search_list)
```
Type|Parameter|Description
---|---|---
`var`|`&$search_list`|desc

### integrate_edit_bans

```php
call_integration_hook('integrate_edit_bans', array(&$ban_info, empty($_REQUEST['bg'])
```
Type|Parameter|Description
---|---|---
`var`|`&$ban_info, empty($_REQUEST['bg']`|desc

### integrate_edit_bans_post

```php
call_integration_hook('integrate_edit_bans_post', array()
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_save_triggers

```php
call_integration_hook('integrate_save_triggers', array(&$ban_triggers, &$ban_group)
```
Type|Parameter|Description
---|---|---
`var`|`&$ban_triggers, &$ban_group`|desc

### integrate_remove_triggers

```php
call_integration_hook('integrate_remove_triggers', array(&$items_ids, $group_id)
```
Type|Parameter|Description
---|---|---
`var`|`&$items_ids, $group_id`|desc

### integrate_manage_boards

```php
call_integration_hook('integrate_manage_boards', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_boards_main

```php
call_integration_hook('integrate_boards_main')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_edit_category

```php
call_integration_hook('integrate_edit_category')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_edit_board

```php
call_integration_hook('integrate_edit_board')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_board_settings

```php
call_integration_hook('integrate_modify_board_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_board_settings

```php
call_integration_hook('integrate_save_board_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_calendar

```php
call_integration_hook('integrate_manage_calendar', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_calendar_settings

```php
call_integration_hook('integrate_modify_calendar_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_calendar_settings

```php
call_integration_hook('integrate_save_calendar_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_languages

```php
call_integration_hook('integrate_manage_languages', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_language_settings

```php
call_integration_hook('integrate_language_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_language_settings

```php
call_integration_hook('integrate_save_language_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_modifylanguages

```php
call_integration_hook('integrate_modifylanguages', array(&$themes, &$lang_dirs, &$allows_add_remove, &$additional_string_types)
```
Type|Parameter|Description
---|---|---
`var`|`&$themes, &$lang_dirs, &$allows_add_remove, &$additional_string_types`|desc

### integrate_language_edit_helptext

```php
call_integration_hook('integrate_language_edit_helptext', array(&$special_groups)
```
Type|Parameter|Description
---|---|---
`var`|`&$special_groups`|desc

### integrate_manage_mail

```php
call_integration_hook('integrate_manage_mail', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_mail_settings

```php
call_integration_hook('integrate_modify_mail_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_mail_settings

```php
call_integration_hook('integrate_save_mail_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_maintenance

```php
call_integration_hook('integrate_manage_maintenance', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_convert_msgbody

```php
call_integration_hook('integrate_convert_msgbody', array($body_type)
```
Type|Parameter|Description
---|---|---
`var`|`$body_type`|desc

### integrate_manage_membergroups

```php
call_integration_hook('integrate_manage_membergroups', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_pre_add_membergroup

```php
call_integration_hook('integrate_pre_add_membergroup', array()
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_add_membergroup

```php
call_integration_hook('integrate_add_membergroup', array($id_group, $postCountBasedGroup)
```
Type|Parameter|Description
---|---|---
`var`|`$id_group, $postCountBasedGroup`|desc

### integrate_save_membergroup

```php
call_integration_hook('integrate_save_membergroup', array((int)
```
Type|Parameter|Description
---|---|---
`var`|`int`|desc

### integrate_view_membergroup

```php
call_integration_hook('integrate_view_membergroup')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_membergroup_settings

```php
call_integration_hook('integrate_modify_membergroup_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_membergroup_settings

```php
call_integration_hook('integrate_save_membergroup_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_members

```php
call_integration_hook('integrate_manage_members', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_view_members_params

```php
call_integration_hook('integrate_view_members_params', array(&$params)
```
Type|Parameter|Description
---|---|---
`var`|`&$params`|desc

### integrate_activate

```php
call_integration_hook('integrate_activate', array($member['username'])
```
Type|Parameter|Description
---|---|---
`var`|`$member['username']`|desc

### integrate_manage_news

```php
call_integration_hook('integrate_manage_news', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_news_settings

```php
call_integration_hook('integrate_modify_news_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_news_settings

```php
call_integration_hook('integrate_save_news_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_subscriptions

```php
call_integration_hook('integrate_manage_subscriptions', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_delete_subscription

```php
call_integration_hook('integrate_delete_subscription', array($context['sub_id'])
```
Type|Parameter|Description
---|---|---
`var`|`$context['sub_id']`|desc

### integrate_save_subscription

```php
call_integration_hook('integrate_save_subscription', array(($context['action_type'] == 'add' ? $id_subscribe : $context['sub_id'])
```
Type|Parameter|Description
---|---|---
`var`|`$context['action_type'] == 'add' ? $id_subscribe : $context['sub_id']`|desc

### integrate_manage_permissions

```php
call_integration_hook('integrate_manage_permissions', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_permission_settings

```php
call_integration_hook('integrate_modify_permission_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_permission_settings

```php
call_integration_hook('integrate_save_permission_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_load_permission_levels

```php
call_integration_hook('integrate_load_permission_levels', array(&$groupLevels, &$boardLevels)
```
Type|Parameter|Description
---|---|---
`var`|`&$groupLevels, &$boardLevels`|desc

### integrate_load_permissions

```php
call_integration_hook('integrate_load_permissions', array(&$permissionGroups, &$permissionList, &$leftPermissionGroups, &$hiddenPermissions, &$relabelPermissions)
```
Type|Parameter|Description
---|---|---
`var`|`&$permissionGroups, &$permissionList, &$leftPermissionGroups, &$hiddenPermissions, &$relabelPermissions`|desc

### integrate_load_illegal_permissions

```php
call_integration_hook('integrate_load_illegal_permissions')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_load_illegal_guest_permissions

```php
call_integration_hook('integrate_load_illegal_guest_permissions')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_post_moderation_mapping

```php
call_integration_hook('integrate_post_moderation_mapping', array(&$mappings)
```
Type|Parameter|Description
---|---|---
`var`|`&$mappings`|desc

### integrate_manage_posts

```php
call_integration_hook('integrate_manage_posts', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_save_censors

```php
call_integration_hook('integrate_save_censors', array(&$updates)
```
Type|Parameter|Description
---|---|---
`var`|`&$updates`|desc

### integrate_censors

```php
call_integration_hook('integrate_censors')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_post_settings

```php
call_integration_hook('integrate_modify_post_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_post_settings

```php
call_integration_hook('integrate_save_post_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_topic_settings

```php
call_integration_hook('integrate_modify_topic_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_topic_settings

```php
call_integration_hook('integrate_save_topic_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_registrations

```php
call_integration_hook('integrate_manage_registrations', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_registration_settings

```php
call_integration_hook('integrate_modify_registration_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_registration_settings

```php
call_integration_hook('integrate_save_registration_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_scheduled_tasks

```php
call_integration_hook('integrate_manage_scheduled_tasks', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_scheduled_tasks_settings

```php
call_integration_hook('integrate_scheduled_tasks_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_scheduled_tasks_settings

```php
call_integration_hook('integrate_save_scheduled_tasks_settings', array(&$save_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$save_vars`|desc

### integrate_manage_search

```php
call_integration_hook('integrate_manage_search', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_search_settings

```php
call_integration_hook('integrate_modify_search_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_search_settings

```php
call_integration_hook('integrate_save_search_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_search_weights

```php
call_integration_hook('integrate_modify_search_weights', array(&$factors)
```
Type|Parameter|Description
---|---|---
`var`|`&$factors`|desc

### integrate_save_search_weights

```php
call_integration_hook('integrate_save_search_weights')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_search_engines

```php
call_integration_hook('integrate_manage_search_engines', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_search_engine_settings

```php
call_integration_hook('integrate_modify_search_engine_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_search_engine_settings

```php
call_integration_hook('integrate_save_search_engine_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_server_settings

```php
call_integration_hook('integrate_server_settings', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_general_settings

```php
call_integration_hook('integrate_general_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_general_settings

```php
call_integration_hook('integrate_save_general_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_database_settings

```php
call_integration_hook('integrate_database_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_database_settings

```php
call_integration_hook('integrate_save_database_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_cookie_settings

```php
call_integration_hook('integrate_cookie_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_cookie_settings

```php
call_integration_hook('integrate_save_cookie_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_general_security_settings

```php
call_integration_hook('integrate_general_security_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_general_security_settings

```php
call_integration_hook('integrate_save_general_security_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_cache_settings

```php
call_integration_hook('integrate_modify_cache_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_cache_settings

```php
call_integration_hook('integrate_save_cache_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_export_settings

```php
call_integration_hook('integrate_export_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_export_settings

```php
call_integration_hook('integrate_save_export_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_loadavg_settings

```php
call_integration_hook('integrate_loadavg_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_loadavg_settings

```php
call_integration_hook('integrate_save_loadavg_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_prepare_db_settings

```php
call_integration_hook('integrate_prepare_db_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_modify_features

```php
call_integration_hook('integrate_modify_features', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_modifications

```php
call_integration_hook('integrate_modify_modifications', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_basic_settings

```php
call_integration_hook('integrate_modify_basic_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_basic_settings

```php
call_integration_hook('integrate_save_basic_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_modify_bbc_settings

```php
call_integration_hook('integrate_modify_bbc_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_bbc_settings

```php
call_integration_hook('integrate_save_bbc_settings', array($bbcTags)
```
Type|Parameter|Description
---|---|---
`var`|`$bbcTags`|desc

### integrate_layout_settings

```php
call_integration_hook('integrate_layout_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_layout_settings

```php
call_integration_hook('integrate_save_layout_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_likes_settings

```php
call_integration_hook('integrate_likes_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_likes_settings

```php
call_integration_hook('integrate_save_likes_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_mentions_settings

```php
call_integration_hook('integrate_mentions_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_mentions_settings

```php
call_integration_hook('integrate_save_mentions_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_warning_settings

```php
call_integration_hook('integrate_warning_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_warning_settings

```php
call_integration_hook('integrate_save_warning_settings', array(&$save_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$save_vars`|desc

### integrate_spam_settings

```php
call_integration_hook('integrate_spam_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_spam_settings

```php
call_integration_hook('integrate_save_spam_settings', array(&$save_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$save_vars`|desc

### integrate_signature_settings

```php
call_integration_hook('integrate_signature_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_apply_signature_settings

```php
call_integration_hook('integrate_apply_signature_settings', array(&$sig, $sig_limits, $disabledTags)
```
Type|Parameter|Description
---|---|---
`var`|`&$sig, $sig_limits, $disabledTags`|desc

### integrate_save_signature_settings

```php
call_integration_hook('integrate_save_signature_settings', array(&$sig_limits, &$bbcTags)
```
Type|Parameter|Description
---|---|---
`var`|`&$sig_limits, &$bbcTags`|desc

### integrate_prune_settings

```php
call_integration_hook('integrate_prune_settings', array(&$config_vars, &$prune_toggle, false)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars, &$prune_toggle, false`|desc

### integrate_prune_settings

```php
call_integration_hook('integrate_prune_settings', array(&$savevar, &$prune_toggle, true)
```
Type|Parameter|Description
---|---|---
`var`|`&$savevar, &$prune_toggle, true`|desc

### integrate_general_mod_settings

```php
call_integration_hook('integrate_general_mod_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_general_mod_settings

```php
call_integration_hook('integrate_save_general_mod_settings', array(&$save_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$save_vars`|desc

### integrate_manage_smileys

```php
call_integration_hook('integrate_manage_smileys', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modify_smiley_settings

```php
call_integration_hook('integrate_modify_smiley_settings', array(&$config_vars)
```
Type|Parameter|Description
---|---|---
`var`|`&$config_vars`|desc

### integrate_save_smiley_settings

```php
call_integration_hook('integrate_save_smiley_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_memberlist_buttons

```php
call_integration_hook('integrate_memberlist_buttons')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### mention_insert_

```php
call_integration_hook('mention_insert_' . $content_type, array($content_id, &$members)
```
Type|Parameter|Description
---|---|---
`var`|`. $content_type, array($content_id, &$members`|desc

### integrate_pre_messageindex

```php
call_integration_hook('integrate_pre_messageindex', array(&$sort_methods, &$sort_methods_table)
```
Type|Parameter|Description
---|---|---
`var`|`&$sort_methods, &$sort_methods_table`|desc

### integrate_message_index

```php
call_integration_hook('integrate_message_index', array(&$message_index_selects, &$message_index_tables, &$message_index_parameters, &$message_index_wheres, &$topic_ids, &$message_index_topic_wheres)
```
Type|Parameter|Description
---|---|---
`var`|`&$message_index_selects, &$message_index_tables, &$message_index_parameters, &$message_index_wheres, &$topic_ids, &$message_index_topic_wheres`|desc

### integrate_quick_mod_actions

```php
call_integration_hook('integrate_quick_mod_actions')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_messageindex_buttons

```php
call_integration_hook('integrate_messageindex_buttons', array(&$context['normal_buttons'])
```
Type|Parameter|Description
---|---|---
`var`|`&$context['normal_buttons']`|desc

### integrate_mod_centre_blocks

```php
call_integration_hook('integrate_mod_centre_blocks', array(&$valid_blocks)
```
Type|Parameter|Description
---|---|---
`var`|`&$valid_blocks`|desc

### integrate_warning_log_actions

```php
call_integration_hook('integrate_warning_log_actions', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_viewModLog

```php
call_integration_hook('integrate_viewModLog', array(&$listOptions, &$moderation_menu_name)
```
Type|Parameter|Description
---|---|---
`var`|`&$listOptions, &$moderation_menu_name`|desc

### integrate_movetopic2_end

```php
call_integration_hook('integrate_movetopic2_end')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_xmlfeeds

```php
call_integration_hook('integrate_xmlfeeds', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_xml_data

```php
call_integration_hook('integrate_xml_data', array(&$xml_data, &$feed_meta, &$namespaces, &$extraFeedTags, &$forceCdataKeys, &$nsKeys, $xml_format, $subaction, &$doctype)
```
Type|Parameter|Description
---|---|---
`var`|`&$xml_data, &$feed_meta, &$namespaces, &$extraFeedTags, &$forceCdataKeys, &$nsKeys, $xml_format, $subaction, &$doctype`|desc

### integrate_fix_url

```php
call_integration_hook('integrate_fix_url', array(&$val)
```
Type|Parameter|Description
---|---|---
`var`|`&$val`|desc

### integrate_package_get

```php
call_integration_hook('integrate_package_get', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_package_download

```php
call_integration_hook('integrate_package_download')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_package_upload

```php
call_integration_hook('integrate_package_upload')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_manage_packages

```php
call_integration_hook('integrate_manage_packages', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_modification_types

```php
call_integration_hook('integrate_modification_types')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_packages_sort_id

```php
call_integration_hook('integrate_packages_sort_id', array(&$sort_id, &$packages)
```
Type|Parameter|Description
---|---|---
`var`|`&$sort_id, &$packages`|desc

### integrate_conversation_buttons

```php
call_integration_hook('integrate_conversation_buttons')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_prepare_pm_context

```php
call_integration_hook('integrate_prepare_pm_context', array(&$output, &$message, $counter)
```
Type|Parameter|Description
---|---|---
`var`|`&$output, &$message, $counter`|desc

### integrate_search_pm_context

```php
call_integration_hook('integrate_search_pm_context')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_pm_post

```php
call_integration_hook('integrate_pm_post')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_pm_error

```php
call_integration_hook('integrate_pm_error')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_poll_vote

```php
call_integration_hook('integrate_poll_vote', array(&$row['id_poll'], &$pollOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$row['id_poll'], &$pollOptions`|desc

### integrate_poll_add_edit

```php
call_integration_hook('integrate_poll_add_edit', array($bcinfo['id_poll'], $isEdit)
```
Type|Parameter|Description
---|---|---
`var`|`$bcinfo['id_poll'], $isEdit`|desc

### integrate_poll_remove

```php
call_integration_hook('integrate_poll_remove', array($pollID)
```
Type|Parameter|Description
---|---|---
`var`|`$pollID`|desc

### integrate_post_start

```php
call_integration_hook('integrate_post_start')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_preview_post

```php
call_integration_hook('integrate_preview_post', array(&$form_message, &$form_subject)
```
Type|Parameter|Description
---|---|---
`var`|`&$form_message, &$form_subject`|desc

### integrate_post_errors

```php
call_integration_hook('integrate_post_errors', array(&$post_errors, &$minor_errors, $form_message, $form_subject)
```
Type|Parameter|Description
---|---|---
`var`|`&$post_errors, &$minor_errors, $form_message, $form_subject`|desc

### integrate_post_end

```php
call_integration_hook('integrate_post_end')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_post2_start

```php
call_integration_hook('integrate_post2_start', array(&$post_errors)
```
Type|Parameter|Description
---|---|---
`var`|`&$post_errors`|desc

### integrate_post2_pre

```php
call_integration_hook('integrate_post2_pre', array(&$post_errors)
```
Type|Parameter|Description
---|---|---
`var`|`&$post_errors`|desc

### integrate_poll_add_edit

```php
call_integration_hook('integrate_poll_add_edit', array($id_poll, false)
```
Type|Parameter|Description
---|---|---
`var`|`$id_poll, false`|desc

### integrate_post2_end

```php
call_integration_hook('integrate_post2_end')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_getTopic_previous_post

```php
call_integration_hook('integrate_getTopic_previous_post', array(&$row)
```
Type|Parameter|Description
---|---|---
`var`|`&$row`|desc

### integrate_post_JavascriptModify

```php
call_integration_hook('integrate_post_JavascriptModify', array(&$post_errors, $row)
```
Type|Parameter|Description
---|---|---
`var`|`&$post_errors, $row`|desc

### integrate_jsmodify_xml

```php
call_integration_hook('integrate_jsmodify_xml')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_post_moderation

```php
call_integration_hook('integrate_post_moderation', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_activate

```php
call_integration_hook('integrate_activate', array($user_profile[$memID]['member_name'])
```
Type|Parameter|Description
---|---|---
`var`|`$user_profile[$memID]['member_name']`|desc

### integrate_export_xslt_variables

```php
call_integration_hook('integrate_export_xslt_variables', array(&$xslt_variables, $format)
```
Type|Parameter|Description
---|---|---
`var`|`&$xslt_variables, $format`|desc

### integrate_export_xslt_stylesheet

```php
call_integration_hook('integrate_export_xslt_stylesheet', array(&$stylesheet, $format)
```
Type|Parameter|Description
---|---|---
`var`|`&$stylesheet, $format`|desc

### integrate_pre_css_output

```php
call_integration_hook('integrate_pre_css_output')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(false)
```
Type|Parameter|Description
---|---|---
`var`|`false`|desc

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(true)
```
Type|Parameter|Description
---|---|---
`var`|`true`|desc

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($cur_profile['member_name'], $value, $_POST['passwrd1'])
```
Type|Parameter|Description
---|---|---
`var`|`$cur_profile['member_name'], $value, $_POST['passwrd1']`|desc

### integrate_load_profile_fields

```php
call_integration_hook('integrate_load_profile_fields', array(&$profile_fields)
```
Type|Parameter|Description
---|---|---
`var`|`&$profile_fields`|desc

### integrate_setup_profile_context

```php
call_integration_hook('integrate_setup_profile_context', array(&$fields)
```
Type|Parameter|Description
---|---|---
`var`|`&$fields`|desc

### integrate_save_custom_profile_fields

```php
call_integration_hook('integrate_save_custom_profile_fields', array(&$changes, &$log_changes, &$errors, $returnErrors, $memID, $area, $sanitize, &$deletes)
```
Type|Parameter|Description
---|---|---
`var`|`&$changes, &$log_changes, &$errors, $returnErrors, $memID, $area, $sanitize, &$deletes`|desc

### integrate_remove_buddy

```php
call_integration_hook('integrate_remove_buddy', array($memID)
```
Type|Parameter|Description
---|---|---
`var`|`$memID`|desc

### integrate_add_buddies

```php
call_integration_hook('integrate_add_buddies', array($memID, &$new_buddies)
```
Type|Parameter|Description
---|---|---
`var`|`$memID, &$new_buddies`|desc

### integrate_view_buddies

```php
call_integration_hook('integrate_view_buddies', array($memID)
```
Type|Parameter|Description
---|---|---
`var`|`$memID`|desc

### integrate_theme_options

```php
call_integration_hook('integrate_theme_options')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_alert_types

```php
call_integration_hook('integrate_alert_types', array(&$alert_types, &$group_options)
```
Type|Parameter|Description
---|---|---
`var`|`&$alert_types, &$group_options`|desc

### integrate_profile_profileSaveGroups

```php
call_integration_hook('integrate_profile_profileSaveGroups', array($value, $additional_groups)
```
Type|Parameter|Description
---|---|---
`var`|`$value, $additional_groups`|desc

### before_profile_save_avatar

```php
call_integration_hook('before_profile_save_avatar', array(&$value)
```
Type|Parameter|Description
---|---|---
`var`|`&$value`|desc

### after_profile_save_avatar

```php
call_integration_hook('after_profile_save_avatar')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_fetch_alerts

```php
call_integration_hook('integrate_fetch_alerts', array(&$alerts, &$formats)
```
Type|Parameter|Description
---|---|---
`var`|`&$alerts, &$formats`|desc

### integrate_profile_showPosts

```php
call_integration_hook('integrate_profile_showPosts')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_profile_stats

```php
call_integration_hook('integrate_profile_stats', array($memID, &$context['text_stats'])
```
Type|Parameter|Description
---|---|---
`var`|`$memID, &$context['text_stats']`|desc

### integrate_profile_trackip

```php
call_integration_hook('integrate_profile_trackip', array($ip_string, $ip_var)
```
Type|Parameter|Description
---|---|---
`var`|`$ip_string, $ip_var`|desc

### integrate_pre_profile_areas

```php
call_integration_hook('integrate_pre_profile_areas', array(&$profile_areas)
```
Type|Parameter|Description
---|---|---
`var`|`&$profile_areas`|desc

### integrate_verify_password

```php
call_integration_hook('integrate_verify_password', array($cur_profile['member_name'], $password, false)
```
Type|Parameter|Description
---|---|---
`var`|`$cur_profile['member_name'], $password, false`|desc

### integrate_profile_save

```php
call_integration_hook('integrate_profile_save', array(&$profile_vars, &$post_errors, $memID, $cur_profile, $current_area)
```
Type|Parameter|Description
---|---|---
`var`|`&$profile_vars, &$post_errors, $memID, $cur_profile, $current_area`|desc

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($cur_profile['member_name'], $cur_profile['member_name'], $_POST['passwrd2'])
```
Type|Parameter|Description
---|---|---
`var`|`$cur_profile['member_name'], $cur_profile['member_name'], $_POST['passwrd2']`|desc

### integrate_profile_popup

```php
call_integration_hook('integrate_profile_popup', array(&$profile_items)
```
Type|Parameter|Description
---|---|---
`var`|`&$profile_items`|desc

### integrate_load_custom_profile_fields

```php
call_integration_hook('integrate_load_custom_profile_fields', array($memID, $area)
```
Type|Parameter|Description
---|---|---
`var`|`$memID, $area`|desc

### integrate_recent_RecentPosts

```php
call_integration_hook('integrate_recent_RecentPosts')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_recent_buttons

```php
call_integration_hook('integrate_recent_buttons')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_unread_list

```php
call_integration_hook('integrate_unread_list')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_activate

```php
call_integration_hook('integrate_activate', array($regOptions['username'])
```
Type|Parameter|Description
---|---|---
`var`|`$regOptions['username']`|desc

### integrate_activate

```php
call_integration_hook('integrate_activate', array($row['member_name'])
```
Type|Parameter|Description
---|---|---
`var`|`$row['member_name']`|desc

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($username, $username, $_POST['passwrd1'])
```
Type|Parameter|Description
---|---|---
`var`|`$username, $username, $_POST['passwrd1']`|desc

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($row['member_name'], $row['member_name'], $_POST['passwrd1'])
```
Type|Parameter|Description
---|---|---
`var`|`$row['member_name'], $row['member_name'], $_POST['passwrd1']`|desc

### integrate_remove_topics_before

```php
call_integration_hook('integrate_remove_topics_before', array($topics, $recycle_board)
```
Type|Parameter|Description
---|---|---
`var`|`$topics, $recycle_board`|desc

### integrate_remove_topics

```php
call_integration_hook('integrate_remove_topics', array($topics)
```
Type|Parameter|Description
---|---|---
`var`|`$topics`|desc

### integrate_remove_message

```php
call_integration_hook('integrate_remove_message', array($message, $row, $recycle)
```
Type|Parameter|Description
---|---|---
`var`|`$message, $row, $recycle`|desc

### integrate_reported_

```php
call_integration_hook('integrate_reported_' . $context['report_type'], array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`. $context['report_type'], array(&$subActions`|desc

### integrate_report_types

```php
call_integration_hook('integrate_report_types')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_report_buttons

```php
call_integration_hook('integrate_report_buttons')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_reports_boardperm

```php
call_integration_hook('integrate_reports_boardperm', array(&$disabled_permissions)
```
Type|Parameter|Description
---|---|---
`var`|`&$disabled_permissions`|desc

### integrate_reports_groupperm

```php
call_integration_hook('integrate_reports_groupperm', array(&$disabled_permissions)
```
Type|Parameter|Description
---|---|---
`var`|`&$disabled_permissions`|desc

### integrate_daily_maintenance

```php
call_integration_hook('integrate_daily_maintenance')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_daily_digest_lang

```php
call_integration_hook('integrate_daily_digest_lang', array(&$langtxt, $lang)
```
Type|Parameter|Description
---|---|---
`var`|`&$langtxt, $lang`|desc

### integrate_daily_digest_email

```php
call_integration_hook('integrate_daily_digest_email', array(&$email, $types, $notify_types, $langtxt)
```
Type|Parameter|Description
---|---|---
`var`|`&$email, $types, $notify_types, $langtxt`|desc

### integrate_weekly_maintenance

```php
call_integration_hook('integrate_weekly_maintenance')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_search

```php
call_integration_hook('integrate_search')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_search_weights

```php
call_integration_hook('integrate_search_weights', array(&$weight_factors)
```
Type|Parameter|Description
---|---|---
`var`|`&$weight_factors`|desc

### integrate_search_sort_columns

```php
call_integration_hook('integrate_search_sort_columns', array(&$sort_columns)
```
Type|Parameter|Description
---|---|---
`var`|`&$sort_columns`|desc

### integrate_search_params

```php
call_integration_hook('integrate_search_params', array(&$search_params)
```
Type|Parameter|Description
---|---|---
`var`|`&$search_params`|desc

### integrate_search_blacklisted_words

```php
call_integration_hook('integrate_search_blacklisted_words', array(&$blacklisted_words)
```
Type|Parameter|Description
---|---|---
`var`|`&$blacklisted_words`|desc

### integrate_search_errors

```php
call_integration_hook('integrate_search_errors')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_subject_only_search_query

```php
call_integration_hook('integrate_subject_only_search_query', array(&$subject_query, &$subject_query_params)
```
Type|Parameter|Description
---|---|---
`var`|`&$subject_query, &$subject_query_params`|desc

### integrate_subject_search_query

```php
call_integration_hook('integrate_subject_search_query', array(&$subject_query)
```
Type|Parameter|Description
---|---|---
`var`|`&$subject_query`|desc

### integrate_main_search_query

```php
call_integration_hook('integrate_main_search_query', array(&$main_query)
```
Type|Parameter|Description
---|---|---
`var`|`&$main_query`|desc

### integrate_search_message_list

```php
call_integration_hook('integrate_search_message_list', array(&$msg_list, &$posters)
```
Type|Parameter|Description
---|---|---
`var`|`&$msg_list, &$posters`|desc

### integrate_quick_mod_actions_search

```php
call_integration_hook('integrate_quick_mod_actions_search')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_search_message_context

```php
call_integration_hook('integrate_search_message_context', array(&$output, &$message, $counter)
```
Type|Parameter|Description
---|---|---
`var`|`&$output, &$message, $counter`|desc

### integrate_validateSession

```php
call_integration_hook('integrate_validateSession', array(&$types)
```
Type|Parameter|Description
---|---|---
`var`|`&$types`|desc

### integrate_verify_password

```php
call_integration_hook('integrate_verify_password', array($user_info['username'], $_POST[$type . '_pass'], false)
```
Type|Parameter|Description
---|---|---
`var`|`$user_info['username'], $_POST[$type . '_pass'], false`|desc

### integrate_post_ban_permissions

```php
call_integration_hook('integrate_post_ban_permissions', array(&$denied_permissions)
```
Type|Parameter|Description
---|---|---
`var`|`&$denied_permissions`|desc

### integrate_warn_permissions

```php
call_integration_hook('integrate_warn_permissions', array(&$permission_change)
```
Type|Parameter|Description
---|---|---
`var`|`&$permission_change`|desc

### integrate_heavy_permissions_session

```php
call_integration_hook('integrate_heavy_permissions_session', array(&$heavy_permissions)
```
Type|Parameter|Description
---|---|---
`var`|`&$heavy_permissions`|desc

### integrate_spam_protection

```php
call_integration_hook('integrate_spam_protection', array(&$timeOverrides)
```
Type|Parameter|Description
---|---|---
`var`|`&$timeOverrides`|desc

### integrate_load_session

```php
call_integration_hook('integrate_load_session')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_session_handlers

```php
call_integration_hook('integrate_session_handlers')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_pre_download_request

```php
call_integration_hook('integrate_pre_download_request')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_download_request

```php
call_integration_hook('integrate_download_request', array(&$attachRequest)
```
Type|Parameter|Description
---|---|---
`var`|`&$attachRequest`|desc

### integrate_split_topic

```php
call_integration_hook('integrate_split_topic', array($split1, $split2, $new_subject, $id_board)
```
Type|Parameter|Description
---|---|---
`var`|`$split1, $split2, $new_subject, $id_board`|desc

### integrate_merge_topic

```php
call_integration_hook('integrate_merge_topic', array($merged_topic, $updated_topics, $deleted_topics, $deleted_polls)
```
Type|Parameter|Description
---|---|---
`var`|`$merged_topic, $updated_topics, $deleted_topics, $deleted_polls`|desc

### integrate_forum_stats

```php
call_integration_hook('integrate_forum_stats')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

./Sources/Subs-Admin.php:904:	if (function_exists('call_integration_hook'))
### integrate_update_settings_file

```php
call_integration_hook('integrate_update_settings_file', array(&$settings_defs)
```
Type|Parameter|Description
---|---|---
`var`|`&$settings_defs`|desc

### integrate_attachment_upload

```php
call_integration_hook('integrate_attachment_upload', array()
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_createAttachment

```php
call_integration_hook('integrate_createAttachment', array(&$attachmentOptions, &$attachmentInserts)
```
Type|Parameter|Description
---|---|---
`var`|`&$attachmentOptions, &$attachmentInserts`|desc

### integrate_assign_attachments

```php
call_integration_hook('integrate_assign_attachments', array(&$attachIDs, &$msgID)
```
Type|Parameter|Description
---|---|---
`var`|`&$attachIDs, &$msgID`|desc

### integrate_pre_parseAttachBBC

```php
call_integration_hook('integrate_pre_parseAttachBBC', array($attachID, $msgID)
```
Type|Parameter|Description
---|---|---
`var`|`$attachID, $msgID`|desc

### integrate_post_parseAttachBBC

```php
call_integration_hook('integrate_post_parseAttachBBC', array(&$attachContext)
```
Type|Parameter|Description
---|---|---
`var`|`&$attachContext`|desc

### integrate_cookie_data

```php
call_integration_hook('integrate_cookie_data', array($data, &$custom_data)
```
Type|Parameter|Description
---|---|---
`var`|`$data, &$custom_data`|desc

### integrate_validateSession

```php
call_integration_hook('integrate_validateSession', array(&$types)
```
Type|Parameter|Description
---|---|---
`var`|`&$types`|desc

### integrate_reset_pass

```php
call_integration_hook('integrate_reset_pass', array($old_user, $user, $newPassword)
```
Type|Parameter|Description
---|---|---
`var`|`$old_user, $user, $newPassword`|desc

### integrate_mod_cache

```php
call_integration_hook('integrate_mod_cache')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_cookie

```php
call_integration_hook('integrate_cookie', array($name, $value, $expire, $path, $domain, $secure, $httponly)
```
Type|Parameter|Description
---|---|---
`var`|`$name, $value, $expire, $path, $domain, $secure, $httponly`|desc

### integrate_pre_boardindex

```php
call_integration_hook('integrate_pre_boardindex', array(&$board_index_selects, &$board_index_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$board_index_selects, &$board_index_parameters`|desc

### integrate_boardindex_board

```php
call_integration_hook('integrate_boardindex_board', array(&$this_category, $row_board)
```
Type|Parameter|Description
---|---|---
`var`|`&$this_category, $row_board`|desc

### integrate_getboardtree

```php
call_integration_hook('integrate_getboardtree', array($board_index_options, &$categories)
```
Type|Parameter|Description
---|---|---
`var`|`$board_index_options, &$categories`|desc

### integrate_getboardtree

```php
call_integration_hook('integrate_getboardtree', array($board_index_options, &$this_category)
```
Type|Parameter|Description
---|---|---
`var`|`$board_index_options, &$this_category`|desc

### integrate_pre_modify_board

```php
call_integration_hook('integrate_pre_modify_board', array($id, &$boardOptions)
```
Type|Parameter|Description
---|---|---
`var`|`$id, &$boardOptions`|desc

### integrate_modify_board

```php
call_integration_hook('integrate_modify_board', array($id, $boardOptions, &$boardUpdates, &$boardUpdateParameters)
```
Type|Parameter|Description
---|---|---
`var`|`$id, $boardOptions, &$boardUpdates, &$boardUpdateParameters`|desc

### integrate_create_board

```php
call_integration_hook('integrate_create_board', array(&$boardOptions, &$board_columns, &$board_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$boardOptions, &$board_columns, &$board_parameters`|desc

### integrate_delete_board

```php
call_integration_hook('integrate_delete_board', array($boards_to_remove, &$moveChildrenTo)
```
Type|Parameter|Description
---|---|---
`var`|`$boards_to_remove, &$moveChildrenTo`|desc

### integrate_pre_boardtree

```php
call_integration_hook('integrate_pre_boardtree', array(&$boardColumns, &$boardParameters, &$boardJoins, &$boardWhere, &$boardOrder)
```
Type|Parameter|Description
---|---|---
`var`|`&$boardColumns, &$boardParameters, &$boardJoins, &$boardWhere, &$boardOrder`|desc

### integrate_boardtree_board

```php
call_integration_hook('integrate_boardtree_board', array($row)
```
Type|Parameter|Description
---|---|---
`var`|`$row`|desc

### integrate_create_event

```php
call_integration_hook('integrate_create_event', array(&$eventOptions, &$event_columns, &$event_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$eventOptions, &$event_columns, &$event_parameters`|desc

### integrate_modify_event

```php
call_integration_hook('integrate_modify_event', array($event_id, &$eventOptions, &$event_columns, &$event_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`$event_id, &$eventOptions, &$event_columns, &$event_parameters`|desc

### integrate_remove_event

```php
call_integration_hook('integrate_remove_event', array($event_id)
```
Type|Parameter|Description
---|---|---
`var`|`$event_id`|desc

### integrate_pre_modify_category

```php
call_integration_hook('integrate_pre_modify_category', array($cat_id, &$catOptions)
```
Type|Parameter|Description
---|---|---
`var`|`$cat_id, &$catOptions`|desc

### integrate_modify_category

```php
call_integration_hook('integrate_modify_category', array($cat_id, &$catUpdates, &$catParameters)
```
Type|Parameter|Description
---|---|---
`var`|`$cat_id, &$catUpdates, &$catParameters`|desc

### integrate_create_category

```php
call_integration_hook('integrate_create_category', array(&$catOptions, &$cat_columns, &$cat_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$catOptions, &$cat_columns, &$cat_parameters`|desc

### integrate_delete_category

```php
call_integration_hook('integrate_delete_category', array($categories, &$moveBoardsTo)
```
Type|Parameter|Description
---|---|---
`var`|`$categories, &$moveBoardsTo`|desc

### integrate_load_message_icons

```php
call_integration_hook('integrate_load_message_icons', array(&$icons)
```
Type|Parameter|Description
---|---|---
`var`|`&$icons`|desc

### integrate_bbc_buttons

```php
call_integration_hook('integrate_bbc_buttons', array(&$context['bbc_tags'], &$editor_tag_map)
```
Type|Parameter|Description
---|---|---
`var`|`&$context['bbc_tags'], &$editor_tag_map`|desc

### integrate_sceditor_options

```php
call_integration_hook('integrate_sceditor_options', array(&$sce_options)
```
Type|Parameter|Description
---|---|---
`var`|`&$sce_options`|desc

### integrate_create_control_verification_pre

```php
call_integration_hook('integrate_create_control_verification_pre', array(&$verificationOptions, $do_test)
```
Type|Parameter|Description
---|---|---
`var`|`&$verificationOptions, $do_test`|desc

### integrate_create_control_verification_test

```php
call_integration_hook('integrate_create_control_verification_test', array($thisVerification, &$verification_errors)
```
Type|Parameter|Description
---|---|---
`var`|`$thisVerification, &$verification_errors`|desc

### integrate_create_control_verification_refresh

```php
call_integration_hook('integrate_create_control_verification_refresh', array($thisVerification)
```
Type|Parameter|Description
---|---|---
`var`|`$thisVerification`|desc

### integrate_create_control_verification_post

```php
call_integration_hook('integrate_create_control_verification_post', array(&$verification_errors, $do_test)
```
Type|Parameter|Description
---|---|---
`var`|`&$verification_errors, $do_test`|desc

### integrate_autosuggest

```php
call_integration_hook('integrate_autosuggest', array(&$searchTypes)
```
Type|Parameter|Description
---|---|---
`var`|`&$searchTypes`|desc

### integrate_

```php
call_integration_hook('integrate_' . $listOptions['id'], array(&$listOptions)
```
Type|Parameter|Description
---|---|---
`var`|`. $listOptions['id'], array(&$listOptions`|desc

### integrate_delete_membergroups

```php
call_integration_hook('integrate_delete_membergroups', array($groups)
```
Type|Parameter|Description
---|---|---
`var`|`$groups`|desc

### integrate_add_members_to_group

```php
call_integration_hook('integrate_add_members_to_group', array($members, $group, &$group_names)
```
Type|Parameter|Description
---|---|---
`var`|`$members, $group, &$group_names`|desc

### integrate_getMembergroupList

```php
call_integration_hook('integrate_getMembergroupList', array(&$groupCache, $group)
```
Type|Parameter|Description
---|---|---
`var`|`&$groupCache, $group`|desc

### integrate_delete_members

```php
call_integration_hook('integrate_delete_members', array($users)
```
Type|Parameter|Description
---|---|---
`var`|`$users`|desc

### integrate_register_check

```php
call_integration_hook('integrate_register_check', array(&$regOptions, &$reg_errors)
```
Type|Parameter|Description
---|---|---
`var`|`&$regOptions, &$reg_errors`|desc

### integrate_register

```php
call_integration_hook('integrate_register', array(&$regOptions, &$theme_vars, &$knownInts, &$knownFloats)
```
Type|Parameter|Description
---|---|---
`var`|`&$regOptions, &$theme_vars, &$knownInts, &$knownFloats`|desc

### integrate_post_register

```php
call_integration_hook('integrate_post_register', array(&$regOptions, &$theme_vars, &$memberID)
```
Type|Parameter|Description
---|---|---
`var`|`&$regOptions, &$theme_vars, &$memberID`|desc

### integrate_register_after

```php
call_integration_hook('integrate_register_after', array($regOptions, $memberID)
```
Type|Parameter|Description
---|---|---
`var`|`$regOptions, $memberID`|desc

### integrate_check_name

```php
call_integration_hook('integrate_check_name', array($checkName, &$is_reserved, $current_id_member, $is_name)
```
Type|Parameter|Description
---|---|---
`var`|`$checkName, &$is_reserved, $current_id_member, $is_name`|desc

### integrate_reattribute_posts

```php
call_integration_hook('integrate_reattribute_posts', array($memID, $email, $membername, $post_count, &$updated)
```
Type|Parameter|Description
---|---|---
`var`|`$memID, $email, $membername, $post_count, &$updated`|desc

### integrate_

```php
call_integration_hook('integrate_' . $menu_context['current_action'] . '_areas', array(&$menuData)
```
Type|Parameter|Description
---|---|---
`var`|`. $menu_context['current_action'] . '_areas', array(&$menuData`|desc

### integrate_preparsecode

```php
call_integration_hook('integrate_preparsecode', array(&$message, $previewing)
```
Type|Parameter|Description
---|---|---
`var`|`&$message, $previewing`|desc

### integrate_unpreparsecode

```php
call_integration_hook('integrate_unpreparsecode', array(&$message)
```
Type|Parameter|Description
---|---|---
`var`|`&$message`|desc

### integrate_outgoing_email

```php
call_integration_hook('integrate_outgoing_email', array(&$subject, &$message, &$headers, &$to_array)
```
Type|Parameter|Description
---|---|---
`var`|`&$subject, &$message, &$headers, &$to_array`|desc

### integrate_personal_message

```php
call_integration_hook('integrate_personal_message', array(&$recipients, &$from, &$subject, &$message)
```
Type|Parameter|Description
---|---|---
`var`|`&$recipients, &$from, &$subject, &$message`|desc

### integrate_personal_message_after

```php
call_integration_hook('integrate_personal_message_after', array(&$id_pm, &$log, &$recipients, &$from, &$subject, &$message)
```
Type|Parameter|Description
---|---|---
`var`|`&$id_pm, &$log, &$recipients, &$from, &$subject, &$message`|desc

### integrate_create_post

```php
call_integration_hook('integrate_create_post', array(&$msgOptions, &$topicOptions, &$posterOptions, &$message_columns, &$message_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$msgOptions, &$topicOptions, &$posterOptions, &$message_columns, &$message_parameters`|desc

### integrate_after_create_post

```php
call_integration_hook('integrate_after_create_post', array($msgOptions, $topicOptions, $posterOptions, $message_columns, $message_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`$msgOptions, $topicOptions, $posterOptions, $message_columns, $message_parameters`|desc

### integrate_before_create_topic

```php
call_integration_hook('integrate_before_create_topic', array(&$msgOptions, &$topicOptions, &$posterOptions, &$topic_columns, &$topic_parameters)
```
Type|Parameter|Description
---|---|---
`var`|`&$msgOptions, &$topicOptions, &$posterOptions, &$topic_columns, &$topic_parameters`|desc

### integrate_create_topic

```php
call_integration_hook('integrate_create_topic', array(&$msgOptions, &$topicOptions, &$posterOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$msgOptions, &$topicOptions, &$posterOptions`|desc

### integrate_modify_topic

```php
call_integration_hook('integrate_modify_topic', array(&$topics_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$topics_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions`|desc

### integrate_modify_post

```php
call_integration_hook('integrate_modify_post', array(&$messages_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions, &$messageInts)
```
Type|Parameter|Description
---|---|---
`var`|`&$messages_columns, &$update_parameters, &$msgOptions, &$topicOptions, &$posterOptions, &$messageInts`|desc

### integrate_after_approve_posts

```php
call_integration_hook('integrate_after_approve_posts', array($approve, $msgs, $topic_changes, $member_post_changes)
```
Type|Parameter|Description
---|---|---
`var`|`$approve, $msgs, $topic_changes, $member_post_changes`|desc

### integrate_get_single_theme

```php
call_integration_hook('integrate_get_single_theme', array(&$themeValues, $id)
```
Type|Parameter|Description
---|---|---
`var`|`&$themeValues, $id`|desc

### integrate_get_all_themes

```php
call_integration_hook('integrate_get_all_themes', array(&$themeValues, $enable_only)
```
Type|Parameter|Description
---|---|---
`var`|`&$themeValues, $enable_only`|desc

### integrate_get_installed_themes

```php
call_integration_hook('integrate_get_installed_themes', array(&$themeValues)
```
Type|Parameter|Description
---|---|---
`var`|`&$themeValues`|desc

### integrate_theme_install

```php
call_integration_hook('integrate_theme_install', array(&$context['to_install'], $id_theme)
```
Type|Parameter|Description
---|---|---
`var`|`&$context['to_install'], $id_theme`|desc

### integrate_change_member_data

```php
call_integration_hook('integrate_change_member_data', array($member_names, $var, &$data[$var], &$knownInts, &$knownFloats)
```
Type|Parameter|Description
---|---|---
`var`|`$member_names, $var, &$data[$var], &$knownInts, &$knownFloats`|desc

### integrate_pre_parsebbc

```php
call_integration_hook('integrate_pre_parsebbc', array(&$message, &$smileys, &$cache_id, &$parse_tags)
```
Type|Parameter|Description
---|---|---
`var`|`&$message, &$smileys, &$cache_id, &$parse_tags`|desc

### integrate_attach_bbc_validate

```php
call_integration_hook('integrate_attach_bbc_validate', array(&$returnContext, $currentAttachment, $tag, $data, $disabled, $params)
```
Type|Parameter|Description
---|---|---
`var`|`&$returnContext, $currentAttachment, $tag, $data, $disabled, $params`|desc

### integrate_bbc_codes

```php
call_integration_hook('integrate_bbc_codes', array(&$codes, &$no_autolink_tags)
```
Type|Parameter|Description
---|---|---
`var`|`&$codes, &$no_autolink_tags`|desc

### integrate_bbc_print

```php
call_integration_hook('integrate_bbc_print', array(&$disabled)
```
Type|Parameter|Description
---|---|---
`var`|`&$disabled`|desc

### integrate_post_parsebbc

```php
call_integration_hook('integrate_post_parsebbc', array(&$message, &$smileys, &$cache_id, &$parse_tags)
```
Type|Parameter|Description
---|---|---
`var`|`&$message, &$smileys, &$cache_id, &$parse_tags`|desc

### integrate_smileys

```php
call_integration_hook('integrate_smileys', array(&$smileyPregSearch, &$smileyPregReplacements)
```
Type|Parameter|Description
---|---|---
`var`|`&$smileyPregSearch, &$smileyPregReplacements`|desc

### integrate_proxy

```php
call_integration_hook('integrate_proxy', array($url, &$proxied_url)
```
Type|Parameter|Description
---|---|---
`var`|`$url, &$proxied_url`|desc

### integrate_redirect

```php
call_integration_hook('integrate_redirect', array(&$setLocation, &$refresh, &$permanent)
```
Type|Parameter|Description
---|---|---
`var`|`&$setLocation, &$refresh, &$permanent`|desc

### integrate_exit

```php
call_integration_hook('integrate_exit', array($do_footer)
```
Type|Parameter|Description
---|---|---
`var`|`$do_footer`|desc

### integrate_theme_context

```php
call_integration_hook('integrate_theme_context')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_security_files

```php
call_integration_hook('integrate_security_files', array(&$securityFiles)
```
Type|Parameter|Description
---|---|---
`var`|`&$securityFiles`|desc

### integrate_pre_javascript_output

```php
call_integration_hook('integrate_pre_javascript_output', array(&$do_deferred)
```
Type|Parameter|Description
---|---|---
`var`|`&$do_deferred`|desc

### integrate_pre_css_output

```php
call_integration_hook('integrate_pre_css_output')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_menu_buttons

```php
call_integration_hook('integrate_menu_buttons', array(&$buttons)
```
Type|Parameter|Description
---|---|---
`var`|`&$buttons`|desc

### integrate_current_action

```php
call_integration_hook('integrate_current_action', array(&$current_action)
```
Type|Parameter|Description
---|---|---
`var`|`&$current_action`|desc

./Sources/Subs.php:5039:function call_integration_hook($hook, $parameters = array())
### integrate_find_like_author

```php
call_integration_hook('integrate_find_like_author', array($this->_details['content_type'], $this->_details['content_id'])
```
Type|Parameter|Description
---|---|---
`var`|`$this->_details['content_type'], $this->_details['content_id']`|desc

### integrate_manage_themes

```php
call_integration_hook('integrate_manage_themes', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_theme_options

```php
call_integration_hook('integrate_theme_options')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_theme_settings

```php
call_integration_hook('integrate_theme_settings')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_wrap_action

```php
call_integration_hook('integrate_wrap_action')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_egg_nog

```php
call_integration_hook('integrate_egg_nog')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### who_allowed

```php
call_integration_hook('who_allowed', array(&$allowedActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$allowedActions`|desc

### integrate_whos_online

```php
call_integration_hook('integrate_whos_online', array($actions)
```
Type|Parameter|Description
---|---|---
`var`|`$actions`|desc

### whos_online_after

```php
call_integration_hook('whos_online_after', array(&$urls, &$data)
```
Type|Parameter|Description
---|---|---
`var`|`&$urls, &$data`|desc

### integrate_credits

```php
call_integration_hook('integrate_credits')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_XMLhttpMain_subActions

```php
call_integration_hook('integrate_XMLhttpMain_subActions', array(&$subActions)
```
Type|Parameter|Description
---|---|---
`var`|`&$subActions`|desc

### integrate_autoload

```php
call_integration_hook('integrate_autoload', array(&$classMap)
```
Type|Parameter|Description
---|---|---
`var`|`&$classMap`|desc

### integrate_SSI

```php
call_integration_hook('integrate_SSI')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_ssi_queryPosts

```php
call_integration_hook('integrate_ssi_queryPosts', array(&$posts)
```
Type|Parameter|Description
---|---|---
`var`|`&$posts`|desc

### integrate_ssi_recentTopics

```php
call_integration_hook('integrate_ssi_recentTopics', array(&$posts)
```
Type|Parameter|Description
---|---|---
`var`|`&$posts`|desc

### integrate_ssi_topPoster

```php
call_integration_hook('integrate_ssi_topPoster', array(&$return)
```
Type|Parameter|Description
---|---|---
`var`|`&$return`|desc

### integrate_ssi_topBoards

```php
call_integration_hook('integrate_ssi_topBoards', array(&$boards)
```
Type|Parameter|Description
---|---|---
`var`|`&$boards`|desc

### integrate_ssi_topTopics

```php
call_integration_hook('integrate_ssi_topTopics', array(&$topics, $type)
```
Type|Parameter|Description
---|---|---
`var`|`&$topics, $type`|desc

### integrate_ssi_queryMembers

```php
call_integration_hook('integrate_ssi_queryMembers', array(&$members)
```
Type|Parameter|Description
---|---|---
`var`|`&$members`|desc

### integrate_ssi_boardStats

```php
call_integration_hook('integrate_ssi_boardStats', array(&$totals)
```
Type|Parameter|Description
---|---|---
`var`|`&$totals`|desc

### integrate_ssi_whosOnline

```php
call_integration_hook('integrate_ssi_whosOnline', array(&$return)
```
Type|Parameter|Description
---|---|---
`var`|`&$return`|desc

### integrate_ssi_recentPoll

```php
call_integration_hook('integrate_ssi_recentPoll', array(&$return, $topPollInstead)
```
Type|Parameter|Description
---|---|---
`var`|`&$return, $topPollInstead`|desc

### integrate_ssi_showPoll

```php
call_integration_hook('integrate_ssi_showPoll', array(&$return)
```
Type|Parameter|Description
---|---|---
`var`|`&$return`|desc

### integrate_ssi_news

```php
call_integration_hook('integrate_ssi_news')
```
Type|Parameter|Description
---|---|---
`var`|``|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$return, $eventOptions`|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$return, $eventOptions`|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$return, $eventOptions`|desc

### integrate_ssi_calendar

```php
call_integration_hook('integrate_ssi_calendar', array(&$return, $eventOptions)
```
Type|Parameter|Description
---|---|---
`var`|`&$return, $eventOptions`|desc

### integrate_ssi_boardNews

```php
call_integration_hook('integrate_ssi_boardNews', array(&$return)
```
Type|Parameter|Description
---|---|---
`var`|`&$return`|desc

### integrate_ssi_recentEvents

```php
call_integration_hook('integrate_ssi_recentEvents', array(&$return)
```
Type|Parameter|Description
---|---|---
`var`|`&$return`|desc

### integrate_ssi_recentAttachments

```php
call_integration_hook('integrate_ssi_recentAttachments', array(&$attachments)
```
Type|Parameter|Description
---|---|---
`var`|`&$attachments`|desc

### integrate_

```php
call_integration_hook('integrate_' . $list_class . '_quickbuttons', array(&$list_items)
```
Type|Parameter|Description
---|---|---
`var`|`. $list_class . '_quickbuttons', array(&$list_items`|desc

### integrate_upload_template

```php
call_integration_hook('integrate_upload_template')
```
Type|Parameter|Description
---|---|---
`var`|``|desc
``````
