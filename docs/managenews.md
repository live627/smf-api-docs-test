---
layout: default
group: func
navtitle: ManageNews.php
title: ./Sources/ManageNews.php
count: 8
---
* auto-gen TOC:
{:toc}
### ManageNews

```php
function ManageNews()
```
The news dispatcher; doesn't do anything, just delegates.

This is the entrance point for all News and Newsletter screens.
Called by ?action=admin;area=news.
It does the permission checks, and calls the appropriate function
based on the requested sub-action.

### EditNews

```php
function EditNews()
```
Let the administrator(s) edit the news items for the forum.

It writes an entry into the moderation log.
This function uses the edit_news administration area.
Called by ?action=admin;area=news.
Requires the edit_news permission.
Can be accessed with ?action=admin;sa=editnews.

Uses a standard list (@see createList())

### list_getNews

```php
function list_getNews()
```
Prepares an array of the forum news items for display in the template



### SelectMailingMembers

```php
function SelectMailingMembers()
```
This function allows a user to select the membergroups to send their
mailing to.

Called by ?action=admin;area=news;sa=mailingmembers.
Requires the send_mail permission.
Form is submitted to ?action=admin;area=news;mailingcompose.

### prepareMailingForPreview

```php
function prepareMailingForPreview()
```
Prepare subject and message of an email for the preview box
Used in ComposeMailing and RetrievePreview (Xml.php)



### ComposeMailing

```php
function ComposeMailing()
```
Shows a form to edit a forum mailing and its recipients.

Called by ?action=admin;area=news;sa=mailingcompose.
Requires the send_mail permission.
Form is submitted to ?action=admin;area=news;sa=mailingsend.

### SendMailing

```php
function SendMailing($clean_only = false)
```
Handles the sending of the forum mailing in batches.

Called by ?action=admin;area=news;sa=mailingsend
Requires the send_mail permission.
Redirects to itself when more batches need to be sent.
Redirects to ?action=admin;area=news;sa=mailingmembers after everything has been sent.

Type|Parameter|Description
---|---|---
`bool`|`$clean_only`|If set, it will only clean the variables, put them in context, then return.

### ModifyNewsSettings

```php
function ModifyNewsSettings($return_config = false)
```
Set general news and newsletter settings and permissions.

Called by ?action=admin;area=news;sa=settings.
Requires the forum_admin permission.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

