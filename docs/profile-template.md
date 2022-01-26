---
layout: default
group: func
navtitle: Profile.template.php
title: ./Themes/default/Profile.template.php
count: 42
---
* auto-gen TOC:
{:toc}
### template_profile_above

```php
function template_profile_above(): void
```
Minor stuff shown above the main profile - mostly used for error messages and showing that the profile update was successful.



### template_profile_below

```php
function template_profile_below(): void
```
Template for any HTML needed below the profile (closing off divs/tables, etc.)



### template_profile_popup

```php
function template_profile_popup(): void
```
Template for showing off the spiffy popup of the menu



### template_alerts_popup

```php
function template_alerts_popup(): void
```
The "popup" showing the user's alerts



### template_alerts_all_read

```php
function template_alerts_all_read(): void
```
A simple template to say "You don't have any unread alerts".



### template_summary

```php
function template_summary(): void
```
This template displays a user's details without any option to edit them.



### template_showPosts

```php
function template_showPosts(): void
```
Template for showing all the posts of the user, in chronological order.



### template_showAlerts

```php
function template_showAlerts(): void
```
Template for showing all alerts



### template_showDrafts

```php
function template_showDrafts(): void
```
Template for showing all of a user's drafts



### template_editBuddies

```php
function template_editBuddies(): void
```
Template for showing and managing the buddy list.



### template_editIgnoreList

```php
function template_editIgnoreList(): void
```
Template for showing the ignore list of the current user.



### template_trackActivity

```php
function template_trackActivity(): void
```
This template shows an admin information on a users IP addresses used and errors attributed to them.



### template_trackIP

```php
function template_trackIP(): void
```
The template for trackIP, allowing the admin to see where/who a certain IP has been used.



### template_showPermissions

```php
function template_showPermissions(): void
```
This template shows an admin which permissions a user have and which group(s) give them each permission.



### template_statPanel

```php
function template_statPanel(): void
```
Template for user statistics, showing graphs and the like.



### template_edit_options

```php
function template_edit_options(): void
```
Template for editing profile options.



### template_profile_pm_settings

```php
function template_profile_pm_settings(): void
```
Personal Message settings.



### template_profile_theme_settings

```php
function template_profile_theme_settings(): void
```
Template for showing theme settings. Note: template_options() actually adds the theme specific options.



### template_alert_configuration

```php
function template_alert_configuration(): void
```
The template for configuring alerts



### template_alert_notifications_topics

```php
function template_alert_notifications_topics(): void
```
Template for showing which topics you're subscribed to



### template_alert_notifications_boards

```php
function template_alert_notifications_boards(): void
```
Template for showing which boards you're subscribed to



### template_groupMembership

```php
function template_groupMembership(): void
```
Template for choosing group membership.



### template_ignoreboards

```php
function template_ignoreboards(): void
```
Template for managing ignored boards



### template_load_warning_variables

```php
function template_load_warning_variables(): void
```
Simply loads some theme variables common to several warning templates.



### template_viewWarning

```php
function template_viewWarning(): void
```
Template for viewing a user's warnings



### template_issueWarning

```php
function template_issueWarning(): void
```
Template for issuing warnings



### template_deleteAccount

```php
function template_deleteAccount(): void
```
Template to show for deleting a user's account - now with added delete post capability!



### template_profile_save

```php
function template_profile_save(): void
```
Template for the password box/save button stuck at the bottom of every profile page.



### template_error_message

```php
function template_error_message(): void
```
Small template for showing an error message upon a save problem in the profile.



### template_profile_group_manage

```php
function template_profile_group_manage(): void
```
Display a load of drop down selectors for allowing the user to change group.



### template_profile_birthdate

```php
function template_profile_birthdate(): void
```
Callback function for entering a birthdate!



### template_profile_signature_modify

```php
function template_profile_signature_modify(): void
```
Show the signature editing box?



### template_profile_avatar_select

```php
function template_profile_avatar_select(): void
```
Template for selecting an avatar



### template_max_size

```php
function template_max_size(string $type): void
```
This is just a really little helper to avoid duplicating code unnecessarily



Type|Parameter|Description
---|---|---
`string`|`$type`|The type of avatar

### template_profile_timeformat_modify

```php
function template_profile_timeformat_modify(): void
```
Select the time format!



### template_profile_theme_pick

```php
function template_profile_theme_pick(): void
```
Template for picking a theme



### template_profile_smiley_pick

```php
function template_profile_smiley_pick(): void
```
Smiley set picker.



### template_tfasetup

```php
function template_tfasetup(): void
```
Template for setting up and managing Two-Factor Authentication.



### template_tfadisable

```php
function template_tfadisable(): void
```
Template for disabling two-factor authentication.



### template_tfasetup_backup

```php
function template_tfasetup_backup(): void
```
Template for setting up 2FA backup code



### template_profile_tfa

```php
function template_profile_tfa(): void
```
Simple template for showing the 2FA area when editing a profile.



### template_export_profile_data

```php
function template_export_profile_data(): void
```
Template for initiating and retrieving profile data exports



