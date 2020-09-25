---
layout: default
group: hooks
title: All Hooks
---

index.php
: integrate_autoload (`&$classMap`)
: integrate_pre_log_stats (`&$no_stat_actions`)
: integrate_actions (`&$actionArray`)

SSI.php
: integrate_autoload (`&$classMap`)
: integrate_SSI
: integrate_ssi_queryPosts (`&$posts`)
: integrate_ssi_recentTopics (`&$posts`)
: integrate_ssi_topPoster (`&$return`)
: integrate_ssi_topBoards (`&$boards`)
: integrate_ssi_topTopics (`&$topics`, `$type`)
: integrate_ssi_queryMembers (`&$members`)
: integrate_ssi_boardStats (`&$totals`)
: integrate_ssi_whosOnline (`&$return`)
: integrate_ssi_recentPoll (`&$return`, `$topPollInstead`)
: integrate_ssi_showPoll (`&$return`)
: integrate_ssi_news
: integrate_ssi_calendar (`&$return`, `$eventOptions`)
: integrate_ssi_calendar (`&$return`, `$eventOptions`)
: integrate_ssi_calendar (`&$return`, `$eventOptions`)
: integrate_ssi_calendar (`&$return`, `$eventOptions`)
: integrate_ssi_boardNews (`&$return`)
: integrate_ssi_recentEvents (`&$return`)
: integrate_ssi_recentAttachments (`&$attachments`)

Sources/Admin.php
: integrate_admin_search (`&$language_files`, `&$include_files`, `&$settings_search`)
: integrate_manage_logs (`&$log_functions`)

Sources/Attachments.php
: integrate_attachment_upload

Sources/BoardIndex.php
: integrate_mark_read_button

Sources/Calendar.php
: integrate_calendar_buttons

Sources/Display.php
: integrate_display_topic (`&$topic_selects`, `&$topic_tables`, `&$topic_parameters`)
: integrate_poll_buttons
: integrate_display_message_list (`&$messages`, `&$posters`)
: integrate_query_message (`&$msg_selects`, `&$msg_tables`, `&$msg_parameters`)
: integrate_display_buttons (`&$context['normal_buttons']`)
: integrate_mod_buttons (`&$context['mod_buttons']`)
: integrate_prepare_display_context (`&$output`, `&$message`, `$counter`)

Sources/Errors.php
: integrate_error_types (`&$other_error_types`, `&$error_type`, `$error_message`, `$file`, `$line`)
: integrate_output_error (`$message`, `$error_type`, `$error_level`, `$file`, `$line`)

Sources/Groups.php
: integrate_manage_groups (`&$subActions`)

Sources/Help.php
: integrate_manage_help (`&$subActions`)
: integrate_helpadmin

Sources/Likes.php
: integrate_valid_likes (`$this->_type`, `$this->_content`, `$this->_sa`, `$this->_js`, `$this->_extra`)
: integrate_issue_like_before (`&$type`, `&$content`, `&$user`, `&$time`)
: integrate_issue_like (`$this`)
: integrate_likes_json_response (`&$print`)

Sources/Load.php
: integrate_load_average (`$modSettings['load_average']`)
: integrate_pre_load
: integrate_verify_user
: integrate_verify_tfa (`$id_member`, `$user_settings`)
: integrate_user_info
: integrate_load_member_data (`&$select_columns`, `&$select_tables`, `&$set`)
: integrate_member_context (`&$memberContext[$user]`, `$user`, `$display_custom_fields`)
: integrate_pre_load_theme (`&$id_theme`)
: integrate_simple_actions (`&$simpleActions`, `&$simpleAreas`, `&$simpleSubActions`, `&$extraParams`, `&$xmlActions`)
: integrate_load_theme
: pre_cache_quick_get (`&$key`, `&$file`, `&$function`, `&$params`, `&$level`)
: post_cache_quick_get (`&$cache_block`)
: cache_put_data (`&$key`, `&$value`, `&$ttl`)
: cache_get_data (`&$key`, `&$ttl`, `&$value`)
: integrate_clean_cache
: integrate_set_avatar_data (`&$image`, `&$data`)

Sources/Logging.php
: integrate_log_types (`&$log_types`)

Sources/LogInOut.php
: integrate_validate_login (`$_POST['user']`, `isset($_POST['passwrd']) ? $_POST['passwrd'] : null`, `$modSettings['cookieTime']`, `true`)
: integrate_other_passwords (`&$other_passwords`)
: integrate_login (`$user_settings['member_name']`, `null`, `$modSettings['cookieTime']`)
: integrate_logout (`$user_settings['member_name']`)

Sources/ManageAttachments.php
: integrate_manage_attachments (`&$subActions`)
: integrate_modify_attachment_settings (`&$config_vars`)
: integrate_save_attachment_settings
: integrate_modify_avatar_settings (`&$config_vars`)
: integrate_save_avatar_settings
: integrate_attachments_browse (`&$listOptions`, `&$titles`, `&$list_title`)
: integrate_attachment_remove (`&$filesRemoved`, `$attachments`)
: integrate_remove_attachments (`$attach`)
: integrate_repair_attachments_nomsg (`&$ignore_ids`, `$_GET['substep']`, `$_GET['substep'] + 500`)
: integrate_approve_attachments (`$attachments`)

Sources/ManageBans.php
: integrate_manage_bans (`&$subActions`)
: integrate_load_addtional_ip_ban (`&$search_list`)

Sources/ManageBoards.php
: integrate_manage_boards (`&$subActions`)
: integrate_boards_main
: integrate_edit_category
: integrate_edit_board
: integrate_modify_board_settings (`&$config_vars`)
: integrate_save_board_settings

Sources/ManageCalendar.php
: integrate_manage_calendar (`&$subActions`)
: integrate_modify_calendar_settings (`&$config_vars`)
: integrate_save_calendar_settings

Sources/ManageLanguages.php
: integrate_manage_languages (`&$subActions`)
: integrate_language_settings (`&$config_vars`)
: integrate_save_language_settings (`&$config_vars`)
: integrate_modifylanguages (`&$themes`, `&$lang_dirs`, `&$allows_add_remove`, `&$additional_string_types`)
: integrate_language_edit_helptext (`&$special_groups`)

Sources/ManageMail.php
: integrate_manage_mail (`&$subActions`)
: integrate_modify_mail_settings (`&$config_vars`)
: integrate_save_mail_settings

Sources/ManageMaintenance.php
: integrate_manage_maintenance (`&$subActions`)
: integrate_convert_msgbody (`$body_type`)

Sources/ManageMembergroups.php
: integrate_manage_membergroups (`&$subActions`)
: integrate_pre_add_membergroup
: integrate_add_membergroup (`$id_group`, `$postCountBasedGroup`)
: integrate_save_membergroup (`(int $_REQUEST['group']`)
: integrate_view_membergroup
: integrate_modify_membergroup_settings (`&$config_vars`)
: integrate_save_membergroup_settings

Sources/ManageMembers.php
: integrate_manage_members (`&$subActions`)
: integrate_view_members_params (`&$params`)
: integrate_activate (`$member['username']`)

Sources/ManageNews.php
: integrate_manage_news (`&$subActions`)
: integrate_modify_news_settings (`&$config_vars`)
: integrate_save_news_settings

Sources/ManagePaid.php
: integrate_manage_subscriptions (`&$subActions`)
: integrate_delete_subscription (`$context['sub_id']`)
: integrate_save_subscription (`($context['action_type'] == 'add' ? $id_subscribe : $context['sub_id'])`, `$_POST['name']`, `$_POST['desc']`, `$isActive`, `$span`, `$cost`, `$_POST['prim_group']`, `$addgroups`, `$isRepeatable`, `$allowpartial`, `$emailComplete`, `$reminder`)

Sources/ManagePermissions.php
: integrate_manage_permissions (`&$subActions`)
: integrate_modify_permission_settings (`&$config_vars`)
: integrate_save_permission_settings
: integrate_load_permission_levels (`&$groupLevels`, `&$boardLevels`)
: integrate_load_permissions (`&$permissionGroups`, `&$permissionList`, `&$leftPermissionGroups`, `&$hiddenPermissions`, `&$relabelPermissions`)
: integrate_load_illegal_permissions
: integrate_load_illegal_guest_permissions
: integrate_post_moderation_mapping (`&$mappings`)

Sources/ManagePosts.php
: integrate_manage_posts (`&$subActions`)
: integrate_save_censors (`&$updates`)
: integrate_censors
: integrate_modify_post_settings (`&$config_vars`)
: integrate_save_post_settings
: integrate_modify_topic_settings (`&$config_vars`)
: integrate_save_topic_settings

Sources/ManageRegistration.php
: integrate_manage_registrations (`&$subActions`)
: integrate_modify_registration_settings (`&$config_vars`)
: integrate_save_registration_settings

Sources/ManageScheduledTasks.php
: integrate_manage_scheduled_tasks (`&$subActions`)
: integrate_scheduled_tasks_settings (`&$config_vars`)
: integrate_save_scheduled_tasks_settings (`&$save_vars`)

Sources/ManageSearch.php
: integrate_manage_search (`&$subActions`)
: integrate_modify_search_settings (`&$config_vars`)
: integrate_save_search_settings
: integrate_modify_search_weights (`&$factors`)
: integrate_save_search_weights

Sources/ManageSearchEngines.php
: integrate_manage_search_engines (`&$subActions`)
: integrate_modify_search_engine_settings (`&$config_vars`)
: integrate_save_search_engine_settings

Sources/ManageServer.php
: integrate_server_settings (`&$subActions`)
: integrate_general_settings (`&$config_vars`)
: integrate_save_general_settings
: integrate_database_settings (`&$config_vars`)
: integrate_save_database_settings
: integrate_cookie_settings (`&$config_vars`)
: integrate_save_cookie_settings
: integrate_general_security_settings (`&$config_vars`)
: integrate_save_general_security_settings
: integrate_modify_cache_settings (`&$config_vars`)
: integrate_save_cache_settings
: integrate_loadavg_settings (`&$config_vars`)
: integrate_save_loadavg_settings
: integrate_prepare_db_settings (`&$config_vars`)

Sources/ManageSettings.php
: integrate_modify_features (`&$subActions`)
: integrate_modify_modifications (`&$subActions`)
: integrate_modify_basic_settings (`&$config_vars`)
: integrate_save_basic_settings
: integrate_modify_bbc_settings (`&$config_vars`)
: integrate_save_bbc_settings (`$bbcTags`)
: integrate_layout_settings (`&$config_vars`)
: integrate_save_layout_settings
: integrate_likes_settings (`&$config_vars`)
: integrate_save_likes_settings
: integrate_mentions_settings (`&$config_vars`)
: integrate_save_mentions_settings
: integrate_warning_settings (`&$config_vars`)
: integrate_save_warning_settings (`&$save_vars`)
: integrate_spam_settings (`&$config_vars`)
: integrate_save_spam_settings (`&$save_vars`)
: integrate_signature_settings (`&$config_vars`)
: integrate_apply_signature_settings (`&$sig`, `$sig_limits`, `$disabledTags`)
: integrate_save_signature_settings (`&$sig_limits`, `&$bbcTags`)
: integrate_prune_settings (`&$config_vars`, `&$prune_toggle`, `false`)
: integrate_prune_settings (`&$savevar`, `&$prune_toggle`, `true`)
: integrate_general_mod_settings (`&$config_vars`)
: integrate_save_general_mod_settings (`&$save_vars`)

Sources/ManageSmileys.php
: integrate_manage_smileys (`&$subActions`)
: integrate_modify_smiley_settings (`&$config_vars`)
: integrate_save_smiley_settings

Sources/Memberlist.php
: integrate_memberlist_buttons

Sources/MessageIndex.php
: integrate_pre_messageindex (`&$sort_methods`, `&$sort_methods_table`)
: integrate_message_index (`&$message_index_selects`, `&$message_index_tables`, `&$message_index_parameters`, `&$message_index_wheres`, `&$topic_ids`)
: integrate_quick_mod_actions
: integrate_messageindex_buttons (`&$context['normal_buttons']`)

Sources/ModerationCenter.php
: integrate_mod_centre_blocks (`&$valid_blocks`)
: integrate_warning_log_actions (`&$subActions`)

Sources/Modlog.php
: integrate_viewModLog (`&$listOptions`, `&$moderation_menu_name`)

Sources/MoveTopic.php
: integrate_movetopic2_end

Sources/News.php
: integrate_xmlfeeds (`&$subActions`)
: integrate_xml_data (`&$xml_data`, `&$feed_meta`, `&$namespaces`, `&$extraFeedTags`, `&$forceCdataKeys`, `&$nsKeys`, `$xml_format`, `$_GET['sa']`)
: integrate_fix_url (`&$val`)

Sources/PackageGet.php
: integrate_package_get (`&$subActions`)
: integrate_package_download
: integrate_package_upload

Sources/Packages.php
: integrate_manage_packages (`&$subActions`)
: integrate_modification_types
: integrate_packages_sort_id (`&$sort_id`, `&$packages`)

Sources/PersonalMessage.php
: integrate_conversation_buttons
: integrate_prepare_pm_context (`&$output`, `&$message`, `$counter`)
: integrate_search_pm_context
: integrate_pm_post
: integrate_pm_error

Sources/Poll.php
: integrate_poll_vote (`&$row['id_poll']`, `&$pollOptions`)
: integrate_poll_add_edit (`$bcinfo['id_poll']`, `$isEdit`)
: integrate_poll_remove (`$pollID`)

Sources/Post.php
: integrate_post_start
: integrate_post_errors (`&$post_errors`, `&$minor_errors`)
: integrate_post_end
: integrate_post2_start
: integrate_poll_add_edit (`$id_poll`, `false`)
: integrate_post2_end

Sources/PostModeration.php
: integrate_post_moderation (`&$subActions`)

Sources/Profile-Actions.php
: integrate_activate (`$user_profile[$memID]['member_name']`)

Sources/Profile-Modify.php
: integrate_reset_pass (`$cur_profile['member_name']`, `$value`, `$_POST['passwrd1']`)
: integrate_load_profile_fields (`&$profile_fields`)
: integrate_setup_profile_context (`&$fields`)
: integrate_save_custom_profile_fields (`&$changes`, `&$log_changes`, `&$errors`, `$returnErrors`, `$memID`, `$area`, `$sanitize`, `&$deletes`)
: integrate_remove_buddy (`$memID`)
: integrate_add_buddies (`$memID`, `&$new_buddies`)
: integrate_view_buddies (`$memID`)
: integrate_theme_options
: integrate_alert_types (`&$alert_types`, `&$group_options`)
: integrate_profile_profileSaveGroups (`$value`, `$additional_groups`)

Sources/Profile-View.php
: integrate_fetch_alerts (`&$alerts`)
: integrate_show_alert (`&$alert`, `&$link`)
: integrate_profile_showPosts
: integrate_profile_stats (`$memID`, `&$context['text_stats']`)
: integrate_profile_trackip (`$ip_string`, `$ip_var`)

Sources/Profile.php
: integrate_pre_profile_areas (`&$profile_areas`)
: integrate_verify_password (`$cur_profile['member_name']`, `$password`, `false`, `true`)
: integrate_profile_save (`&$profile_vars`, `&$post_errors`, `$memID`, `$cur_profile`, `$current_area`)
: integrate_reset_pass (`$cur_profile['member_name']`, `$cur_profile['member_name']`, `$_POST['passwrd2']`)
: integrate_profile_popup (`&$profile_items`)
: integrate_load_custom_profile_fields (`$memID`, `$area`)

Sources/Recent.php
: integrate_recent_RecentPosts
: integrate_recent_buttons
: integrate_unread_list

Sources/Register.php
: integrate_activate (`$regOptions['username']`)
: integrate_activate (`$row['member_name']`)

Sources/Reminder.php
: integrate_reset_pass (`$username`, `$username`, `$_POST['passwrd1']`)
: integrate_reset_pass (`$row['member_name']`, `$row['member_name']`, `$_POST['passwrd1']`)

Sources/RemoveTopic.php
: integrate_remove_topics (`$topics`)
: integrate_remove_message (`$message`)

Sources/Reports.php
: integrate_report_types
: integrate_report_buttons
: integrate_reports_boardperm (`&$disabled_permissions`)
: integrate_reports_groupperm (`&$disabled_permissions`)

Sources/Search.php
: integrate_search
: integrate_search_weights (`&$weight_factors`)
: integrate_search_sort_columns (`&$sort_columns`)
: integrate_search_params (`&$search_params`)
: integrate_search_blacklisted_words (`&$blacklisted_words`)
: integrate_search_errors
: integrate_subject_only_search_query (`&$subject_query`, `&$subject_query_params`)
: integrate_subject_search_query (`&$subject_query`)
: integrate_main_search_query (`&$main_query`)
: integrate_search_message_list (`&$msg_list`, `&$posters`)
: integrate_quick_mod_actions_search
: integrate_search_message_context (`&$output`, `&$message`, `$counter`)

Sources/Security.php
: integrate_validateSession (`&$types`)
: integrate_verify_password (`$user_info['username']`, `$_POST[$type . '_pass']`, `false`, `true`)
: integrate_post_ban_permissions (`&$denied_permissions`)
: integrate_warn_permissions (`&$permission_change`)
: integrate_heavy_permissions_session (`&$heavy_permissions`)
: integrate_spam_protection (`&$timeOverrides`)

Sources/Session.php
: integrate_session_handlers

Sources/ShowAttachments.php
: integrate_pre_download_request
: integrate_download_request (`&$attachRequest`)

Sources/SplitTopics.php
: integrate_split_topic (`$split1`, `$split2`, `$new_subject`, `$id_board`)
: integrate_merge_topic (`$merged_topic`, `$updated_topics`, `$deleted_topics`, `$deleted_polls`)

Sources/Stats.php
: integrate_forum_stats

Sources/Subs-Attachments.php
: integrate_attachment_upload
: integrate_createAttachment (`&$attachmentOptions`, `&$attachmentInserts`)
: integrate_assign_attachments (`&$attachIDs`, `&$msgID`)
: integrate_pre_parseAttachBBC (`$attachID`, `$msgID`)
: integrate_post_parseAttachBBC (`&$attachContext`)

Sources/Subs-Auth.php
: integrate_cookie_data (`$data`, `&$custom_data`)
: integrate_validateSession (`&$types`)
: integrate_reset_pass (`$old_user`, `$user`, `$newPassword`)
: integrate_mod_cache
: integrate_cookie (`$name`, `$value`, `$expire`, `$path`, `$domain`, `$secure`, `$httponly`)

Sources/Subs-BoardIndex.php
: integrate_getboardtree (`$boardIndexOptions`, `&$categories`)
: integrate_getboardtree (`$boardIndexOptions`, `&$this_category`)

Sources/Subs-Boards.php
: integrate_pre_modify_board (`$id`, `&$boardOptions`)
: integrate_modify_board (`$id`, `$boardOptions`, `&$boardUpdates`, `&$boardUpdateParameters`)
: integrate_create_board (`&$boardOptions`, `&$board_columns`, `&$board_parameters`)
: integrate_delete_board (`$boards_to_remove`, `&$moveChildrenTo`)
: integrate_pre_boardtree (`&$boardColumns`, `&$boardParameters`, `&$boardJoins`, `&$boardWhere`, `&$boardOrder`)
: integrate_boardtree_board (`$row`)

Sources/Subs-Calendar.php
: integrate_create_event (`&$eventOptions`, `&$event_columns`, `&$event_parameters`)
: integrate_modify_event (`$event_id`, `&$eventOptions`, `&$event_columns`, `&$event_parameters`)
: integrate_remove_event (`$event_id`)

Sources/Subs-Categories.php
: integrate_pre_modify_category (`$cat_id`, `&$catOptions`)
: integrate_modify_category (`$cat_id`, `&$catUpdates`, `&$catParameters`)
: integrate_create_category (`&$catOptions`, `&$cat_columns`, `&$cat_parameters`)
: integrate_delete_category (`$categories`, `&$moveBoardsTo`)

Sources/Subs-Editor.php
: integrate_load_message_icons (`&$icons`)
: integrate_bbc_buttons (`&$context['bbc_tags']`, `&$editor_tag_map`)
: integrate_sceditor_options (`&$sce_options`)
: integrate_autosuggest (`&$searchTypes`)

Sources/Subs-Membergroups.php
: integrate_delete_membergroups (`$groups`)
: integrate_add_members_to_group (`$members`, `$group`, `&$group_names`)

Sources/Subs-Members.php
: integrate_delete_members (`$users`)
: integrate_register_check (`&$regOptions`, `&$reg_errors`)
: integrate_register (`&$regOptions`, `&$theme_vars`, `&$knownInts`, `&$knownFloats`)
: integrate_post_register (`&$regOptions`, `&$theme_vars`, `&$memberID`)
: integrate_register_after (`$regOptions`, `$memberID`)
: integrate_reattribute_posts (`$memID`, `$email`, `$membername`, `$post_count`, `&$updated`)

Sources/Subs-Post.php
: integrate_outgoing_email (`&$subject`, `&$message`, `&$headers`, `&$to_array`, `true`)
: integrate_personal_message (`&$recipients`, `&$from`, `&$subject`, `&$message`)
: integrate_personal_message_after (`&$id_pm`, `&$log`, `&$recipients`, `&$from`, `&$subject`, `&$message`)
: integrate_create_post (`&$msgOptions`, `&$topicOptions`, `&$posterOptions`, `&$message_columns`, `&$message_parameters`)
: integrate_after_create_post (`$msgOptions`, `$topicOptions`, `$posterOptions`, `$message_columns`, `$message_parameters`)
: integrate_before_create_topic (`&$msgOptions`, `&$topicOptions`, `&$posterOptions`, `&$topic_columns`, `&$topic_parameters`)
: integrate_create_topic (`&$msgOptions`, `&$topicOptions`, `&$posterOptions`)
: integrate_modify_topic (`&$topics_columns`, `&$update_parameters`, `&$msgOptions`, `&$topicOptions`, `&$posterOptions`)
: integrate_modify_post (`&$messages_columns`, `&$update_parameters`, `&$msgOptions`, `&$topicOptions`, `&$posterOptions`, `&$messageInts`)

Sources/Subs-Themes.php
: integrate_get_single_theme (`&$themeValues`, `$id`)
: integrate_get_all_themes (`&$themeValues`, `$enable_only`)
: integrate_get_installed_themes (`&$themeValues`)
: integrate_theme_install (`&$context['to_install']`, `$id_theme`)

Sources/Subs.php
: integrate_change_member_data (`$member_names`, `$var`, `&$data[$var]`, `&$knownInts`, `&$knownFloats`)
: integrate_pre_parsebbc (`&$message`, `&$smileys`, `&$cache_id`, `&$parse_tags`)
: integrate_bbc_codes (`&$codes`, `&$no_autolink_tags`)
: integrate_bbc_print (`&$disabled`)
: integrate_post_parsebbc (`&$message`, `&$smileys`, `&$cache_id`, `&$parse_tags`)
: integrate_smileys (`&$smileyPregSearch`, `&$smileyPregReplacements`)
: integrate_proxy (`$url`, `&$proxied_url`)
: integrate_redirect (`&$setLocation`, `&$refresh`, `&$permanent`)
: integrate_exit (`$do_footer`)
: integrate_theme_context
: integrate_security_files (`&$securityFiles`)
: integrate_pre_javascript_output (`&$do_deferred`)
: integrate_pre_css_output
: integrate_menu_buttons (`&$buttons`)
: integrate_current_action (`&$current_action`)

Sources/Themes.php
: integrate_manage_themes (`&$subActions`)
: integrate_theme_options
: integrate_theme_settings
: integrate_wrap_action

Sources/Who.php
: who_allowed (`&$allowedActions`)
: integrate_whos_online (`$actions > 0`)
: whos_online_after (`&$urls`, `&$data`)
: integrate_credits

Sources/Xml.php
: integrate_XMLhttpMain_subActions (`&$subActions`)

Sources/tasks/Likes-Notify.php
: integrate_find_like_author (`$this->_details['content_type']`, `$this->_details['content_id']`)

Themes/default/Post.template.php
: integrate_upload_template
