---
layout: default
group: func
navtitle: MoveTopic.php
title: ./Sources/MoveTopic.php
count: 4
---
* auto-gen TOC:
{:toc}
### MoveTopic

```php
function MoveTopic(): void
```
This function allows to move a topic, making sure to ask the moderator
to give reason for topic move.

It must be called with a topic specified. (that is, global $topic must
be set... @todo fix this thing.)
If the member is the topic starter requires the move_own permission,
otherwise the move_any permission.
Accessed via ?action=movetopic.

Uses the MoveTopic template, main sub-template.

### MoveTopic2

```php
function MoveTopic2(): void
```
Execute the move of a topic.

It is called on the submit of MoveTopic.
This function logs that topics have been moved in the moderation log.
If the member is the topic starter requires the move_own permission,
otherwise requires the move_any permission.
Upon successful completion redirects to message index.
Accessed via ?action=movetopic2.

Uses Subs-Post.php

Integration hooks
: integrate_movetopic2_end

### moveTopics

```php
function moveTopics(int|int[] $topics, int $toBoard): void
```
Moves one or more topics to a specific board. (doesn't check permissions.)
Determines the source boards for the supplied topics
Handles the moving of mark_read data
Updates the posts count of the affected boards



Type|Parameter|Description
---|---|---
`int` &#124; `int[]`|`$topics`|The ID of a single topic to move or an array containing the IDs of multiple topics to move
`int`|`$toBoard`|The ID of the board to move the topics to

### moveTopicConcurrence

```php
function moveTopicConcurrence(): void
```
Called after a topic is moved to update $board_link and $topic_link to point to new location



