---
layout: default
group: func
navtitle: Post.php
title: ./Sources/Post.php
count: 8
---
* auto-gen TOC:
{:toc}
### Post

```php
function Post($post_errors = array())
```
Handles showing the post screen, loading the post to be modified, and loading any post quoted.

- additionally handles previews of posts.
- Uses the Post template and language file, main sub template.
- requires different permissions depending on the actions, but most notably post_new, post_reply_own, and post_reply_any.
- shows options for the editing and posting of calendar events and attachments, as well as the posting of polls.
- accessed from ?action=post.

Type|Parameter|Description
---|---|---
`array`|`$post_errors`|Holds any errors found while tyring to post

### Post2

```php
function Post2()
```
Posts or saves the message composed with Post().

requires various permissions depending on the action.
handles attachment, post, and calendar saving.
sends off notifications, and allows for announcements and moderation.
accessed from ?action=post2.

### AnnounceTopic

```php
function AnnounceTopic()
```
Handle the announce topic function (action=announce).

checks the topic announcement permissions and loads the announcement template.
requires the announce_topic permission.
uses the ManageMembers template and Post language file.
call the right function based on the sub-action.

### AnnouncementSelectMembergroup

```php
function AnnouncementSelectMembergroup()
```
Allow a user to chose the membergroups to send the announcement to.

lets the user select the membergroups that will receive the topic announcement.

### AnnouncementSend

```php
function AnnouncementSend()
```
Send the announcement in chunks.

splits the members to be sent a topic announcement into chunks.
composes notification messages in all languages needed.
does the actual sending of the topic announcements in chunks.
calculates a rough estimate of the percentage items sent.

### getTopic

```php
function getTopic()
```
Get the topic for display purposes.

gets a summary of the most recent posts in a topic.
depends on the topicSummaryPosts setting.
if you are editing a post, only shows posts previous to that post.

### QuoteFast

```php
function QuoteFast()
```
Loads a post an inserts it into the current editing text box.

uses the Post language file.
uses special (sadly browser dependent) javascript to parse entities for internationalization reasons.
accessed with ?action=quotefast.

### JavaScriptModify

```php
function JavaScriptModify()
```
Used to edit the body or subject of a message inline
called from action=jsmodify from script and topic js



