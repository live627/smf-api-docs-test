---
layout: default
group: func
navtitle: Display.php
title: ./Sources/Display.php
count: 4
---
* auto-gen TOC:
{:toc}
### Display

```php
function Display(): void
```
The central part of the board - topic display.

This function loads the posts in a topic up so they can be displayed.
It uses the main sub template of the Display template.
It requires a topic, and can go to the previous or next topic from it.
It jumps to the correct post depending on a number/time/IS_MSG passed.
It depends on the messages_per_page, defaultMaxMessages and enableAllMessages settings.
It is accessed by ?topic=id_topic.START.

Integration hooks
: integrate_display_topic
: integrate_poll_buttons
: integrate_display_message_list
: integrate_query_message
: integrate_display_buttons
: integrate_mod_buttons

### prepareDisplayContext

```php
function prepareDisplayContext(bool $reset = false): array
```
Callback for the message display.

It actually gets and prepares the message context.
This function will start over from the beginning if reset is set to true, which is
useful for showing an index before or after the posts.

Type|Parameter|Description
---|---|---
`bool`|`$reset`|Whether or not to reset the db seek pointer

Integration hooks
: integrate_prepare_display_context

### Download

```php
function Download(): void
```
Once upon a time, this function handled downloading attachments.

Now it's just an alias retained for the sake of backwards compatibility.

### QuickInTopicModeration

```php
function QuickInTopicModeration(): void
```
In-topic quick moderation.



