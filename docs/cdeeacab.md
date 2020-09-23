---
layout: default
title: Display.php
count: 4
---

# ./Sources/Display.php

### Display

```php
function Display()
```
The central part of the board - topic display.

This function loads the posts in a topic up so they can be displayed.
It uses the main sub template of the Display template.
It requires a topic, and can go to the previous or next topic from it.
It jumps to the correct post depending on a number/time/IS_MSG passed.
It depends on the messages_per_page, defaultMaxMessages and enableAllMessages settings.
It is accessed by ?topic=id_topic.START.

### prepareDisplayContext

```php
function prepareDisplayContext($reset = false)
```
Callback for the message display.

It actually gets and prepares the message context.
This function will start over from the beginning if reset is set to true, which is
useful for showing an index before or after the posts.

Type|Parameter|Name
---|---|---
bool|$reset|Whether or not to reset the db seek pointer
### Download

```php
function Download()
```
Once upon a time, this function handled downloading attachments.

Now it's just an alias retained for the sake of backwards compatibility.

### QuickInTopicModeration

```php
function QuickInTopicModeration()
```
In-topic quick moderation.



