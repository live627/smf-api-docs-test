---
layout: default
group: func
navtitle: ModerationCenter.template.php
title: ./Themes/default/ModerationCenter.template.php
count: 11
---
* auto-gen TOC:
{:toc}
### template_moderation_center

```php
function template_moderation_center(): void
```
The main moderation center.



### template_group_requests_block

```php
function template_group_requests_block(): void
```
Show all the group requests the user can see.



### template_watched_users

```php
function template_watched_users(): void
```
A list of watched users



### template_reported_posts_block

```php
function template_reported_posts_block(): void
```
A list of reported posts



### template_reported_users_block

```php
function template_reported_users_block(): void
```
A list of reported users



### template_notes

```php
function template_notes(): void
```
Little section for making... notes.



### template_unapproved_posts

```php
function template_unapproved_posts(): void
```
Show a list of all the unapproved posts



### template_user_watch_post_callback

```php
function template_user_watch_post_callback(array $post): string
```
Callback function for showing a watched users post in the table.



Type|Parameter|Description
---|---|---
`array`|`$post`|An array of data about the post.

### template_moderation_settings

```php
function template_moderation_settings(): void
```
The moderation settings page.



### template_show_notice

```php
function template_show_notice(): void
```
Show a notice sent to a user.



### template_warn_template

```php
function template_warn_template(): void
```
Add or edit a warning template.



