---
layout: default
group: func
navtitle: Subs-Post.php
title: ./Sources/Subs-Post.php
count: 23
---
* auto-gen TOC:
{:toc}
### preparsecode

```php
function preparsecode(&$message, $previewing = false)
```
Takes a message and parses it, returning nothing.

Cleans up links (javascript, etc.) and code/quote sections.
Won't convert \n's and a few other things if previewing is true.

Type|Parameter|Description
---|---|---
`string`|`$message`|The mesasge
`bool`|`$previewing`|Whether we're previewing

### un_preparsecode

```php
function un_preparsecode($message)
```
This is very simple, and just removes things done by preparsecode.



Type|Parameter|Description
---|---|---
`string`|`$message`|The message

### fixTags

```php
function fixTags(&$message)
```
Fix any URLs posted - ie. remove 'javascript:'.

Used by preparsecode, fixes links in message and returns nothing.

Type|Parameter|Description
---|---|---
`string`|`$message`|The message

### fixTag

```php
function fixTag(&$message, $myTag, $protocols, $embeddedUrl = false, $hasEqualSign = false, $hasExtra = false)
```
Fix a specific class of tag - ie. url with =.

Used by fixTags, fixes a specific tag's links.

Type|Parameter|Description
---|---|---
`string`|`$message`|The message
`string`|`$myTag`|The tag
`string`|`$protocols`|The protocols
`bool`|`$embeddedUrl`|Whether it *can* be set to something
`bool`|`$hasEqualSign`|Whether it *is* set to something
`bool`|`$hasExtra`|Whether it can have extra cruft after the begin tag.

### sendmail

```php
function sendmail($to, $subject, $message, $from = null, $message_id = null, $send_html = false, $priority = 3, $hotmail_fix = null, $is_private = false)
```
This function sends an email to the specified recipient(s).

It uses the mail_type settings and webmaster_email variable.

Type|Parameter|Description
---|---|---
`array`|`$to`|The email(s) to send to
`string`|`$subject`|Email subject, expected to have entities, and slashes, but not be parsed
`string`|`$message`|Email body, expected to have slashes, no htmlentities
`string`|`$from`|The address to use for replies
`string`|`$message_id`|If specified, it will be used as local part of the Message-ID header.
`bool`|`$send_html`|Whether or not the message is HTML vs. plain text
`int`|`$priority`|The priority of the message
`bool`|`$hotmail_fix`|Whether to apply the "hotmail fix"
`bool`|`$is_private`|Whether this is private

### AddMailQueue

```php
function AddMailQueue($flush = false, $to_array = array(), $subject = '', $message = '', $headers = '', $send_html = false, $priority = 3, $is_private = false)
```
Add an email to the mail queue.



Type|Parameter|Description
---|---|---
`bool`|`$flush`|Whether to flush the queue
`array`|`$to_array`|An array of recipients
`string`|`$subject`|The subject of the message
`string`|`$message`|The message
`string`|`$headers`|The headers
`bool`|`$send_html`|Whether to send in HTML format
`int`|`$priority`|The priority
`bool`|`$is_private`|Whether this is private

### sendpm

```php
function sendpm($recipients, $subject, $message, $store_outbox = false, $from = null, $pm_head = 0)
```
Sends an personal message from the specified person to the specified people
($from defaults to the user)



Type|Parameter|Description
---|---|---
`array`|`$recipients`|An array containing the arrays 'to' and 'bcc', both containing id_member's.
`string`|`$subject`|Should have no slashes and no html entities
`string`|`$message`|Should have no slashes and no html entities
`bool`|`$store_outbox`|Whether to store it in the sender's outbox
`array`|`$from`|An array with the id, name, and username of the member.
`int`|`$pm_head`|The ID of the chain being replied to - if any.

### mimespecialchars

```php
function mimespecialchars($string, $with_charset = true, $hotmail_fix = false, $line_break = "\r\n", $custom_charset = null)
```
Prepare text strings for sending as email body or header.

In case there are higher ASCII characters in the given string, this
function will attempt the transport method 'quoted-printable'.
Otherwise the transport method '7bit' is used.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string
`bool`|`$with_charset`|Whether we're specifying a charset ($custom_charset must be set here)
`bool`|`$hotmail_fix`|Whether to apply the hotmail fix  (all higher ASCII characters are converted to HTML entities to assure proper display of the mail)
`string`|`$line_break`|The linebreak
`string`|`$custom_charset`|If set, it uses this character set

### smtp_mail

```php
function smtp_mail($mail_to_array, $subject, $message, $headers)
```
Sends mail, like mail() but over SMTP.

It expects no slashes or entities.

Type|Parameter|Description
---|---|---
`array`|`$mail_to_array`|Array of strings (email addresses)
`string`|`$subject`|Email subject
`string`|`$message`|Email message
`string`|`$headers`|Email headers

### server_parse

```php
function server_parse($message, $socket, $code, &$response = null)
```
Parse a message to the SMTP server.

Sends the specified message to the server, and checks for the
expected response.

Type|Parameter|Description
---|---|---
`string`|`$message`|The message to send
`resource`|`$socket`|Socket to send on
`string`|`$code`|The expected response code
`string`|`$response`|The response from the SMTP server

### SpellCheck

```php
function SpellCheck()
```
Spell checks the post for typos ;).

It uses the pspell or enchant library, one of which MUST be installed.
It has problems with internationalization.
It is accessed via ?action=spellcheck.

### sendNotifications

```php
function sendNotifications($topics, $type, $exclude = array(), $members_only = array())
```
Sends a notification to members who have elected to receive emails
when things happen to a topic, such as replies are posted.

The function automatically finds the subject and its board, and
checks permissions for each member who is "signed up" for notifications.
It will not send 'reply' notifications more than once in a row.
Uses Post language file

Type|Parameter|Description
---|---|---
`array`|`$topics`|Represents the topics the action is happening to.
`string`|`$type`|Can be any of reply, sticky, lock, unlock, remove, move, merge, and split.  An appropriate message will be sent for each.
`array`|`$exclude`|Members in the exclude array will not be processed for the topic with the same key.
`array`|`$members_only`|Are the only ones that will be sent the notification if they have it on.

### createPost

```php
function createPost(&$msgOptions, &$topicOptions, &$posterOptions)
```
Create a post, either as new topic (id_topic = 0) or in an existing one.

The input parameters of this function assume:
- Strings have been escaped.
- Integers have been cast to integer.
- Mandatory parameters are set.

Type|Parameter|Description
---|---|---
`array`|`$msgOptions`|An array of information/options for the post
`array`|`$topicOptions`|An array of information/options for the topic
`array`|`$posterOptions`|An array of information/options for the poster

### modifyPost

```php
function modifyPost(&$msgOptions, &$topicOptions, &$posterOptions)
```
Modifying a post.

..

Type|Parameter|Description
---|---|---
`array`|` &$msgOptions`|An array of information/options for the post
`array`|` &$topicOptions`|An array of information/options for the topic
`array`|` &$posterOptions`|An array of information/options for the poster

### approvePosts

```php
function approvePosts($msgs, $approve = true, $notify = true)
```
Approve (or not) some posts... without permission checks.

..

Type|Parameter|Description
---|---|---
`array`|`$msgs`|Array of message ids
`bool`|`$approve`|Whether to approve the posts (if false, posts are unapproved)
`bool`|`$notify`|Whether to notify users

### approveTopics

```php
function approveTopics($topics, $approve = true)
```
Approve topics?



Type|Parameter|Description
---|---|---
`array`|`$topics`|Array of topic ids
`bool`|`$approve`|Whether to approve the topics. If false, unapproves them instead

### updateLastMessages

```php
function updateLastMessages($setboards, $id_msg = 0)
```
Takes an array of board IDs and updates their last messages.

If the board has a parent, that parent board is also automatically
updated.
The columns updated are id_last_msg and last_updated.
Note that id_last_msg should always be updated using this function,
and is not automatically updated upon other changes.

Type|Parameter|Description
---|---|---
`array`|`$setboards`|An array of board IDs
`int`|`$id_msg`|The ID of the message

### adminNotify

```php
function adminNotify($type, $memberID, $member_name = null)
```
This simple function gets a list of all administrators and sends them an email
 to let them know a new member has joined.

Called by registerMember() function in Subs-Members.php.
Email is sent to all groups that have the moderate_forum permission.
The language set by each member is being used (if available).
Uses the Login language file

Type|Parameter|Description
---|---|---
`string`|`$type`|The type. Types supported are 'approval', 'activation', and 'standard'.
`int`|`$memberID`|The ID of the member
`string`|`$member_name`|The name of the member (if null, it is pulled from the database)

### loadEmailTemplate

```php
function loadEmailTemplate($template, $replacements = array(), $lang = '', $loadLang = true)
```
Load a template from EmailTemplates language file.



Type|Parameter|Description
---|---|---
`string`|`$template`|The name of the template to load
`array`|`$replacements`|An array of replacements for the variables in the template
`string`|`$lang`|The language to use, if different than the user's current language
`bool`|`$loadLang`|Whether to load the language file first

### user_info_callback

```php
function user_info_callback($matches)
```
Callback function for loademaitemplate on subject and body
Uses capture group 1 in array



Type|Parameter|Description
---|---|---
`array`|`$matches`|An array of matches

### spell_init

```php
function spell_init()
```
spell_init()

Sets up a dictionary resource handle. Tries enchant first then falls through to pspell.

### spell_check

```php
function spell_check($dict, $word)
```
spell_check()

Determines whether or not the specified word is spelled correctly

Type|Parameter|Description
---|---|---
`resource`|`$dict`|An enchant or pspell dictionary resource set up by {@link spell_init()}
`string`|`$word`|A word to check the spelling of

### spell_suggest

```php
function spell_suggest($dict, $word)
```
spell_suggest()

Returns an array of suggested replacements for the specified word

Type|Parameter|Description
---|---|---
`resource`|`$dict`|An enchant or pspell dictionary resource
`string`|`$word`|A misspelled word

