---
layout: default
group: func
navtitle: RemoveTopic.php
title: ./Sources/RemoveTopic.php
count: 8
---
* auto-gen TOC:
{:toc}
### RemoveTopic2

```php
function RemoveTopic2(): void
```
Completely remove an entire topic.

Redirects to the board when completed.

### DeleteMessage

```php
function DeleteMessage(): void
```
Remove just a single post.

On completion redirect to the topic or to the board.

### RemoveOldTopics2

```php
function RemoveOldTopics2(): void
```
So long as you are sure... all old posts will be gone.

Used in ManageMaintenance.php to prune old topics.

### removeTopics

```php
function removeTopics(array|int $topics, bool $decreasePostCount = true, bool $ignoreRecycling = false, bool $updateBoardCount = true): void
```
Removes the passed id_topic's. (permissions are NOT checked here!).



Type|Parameter|Description
---|---|---
`array` &#124; `int`|`$topics`|The topics to remove \(can be an id or an array of ids\)\.
`bool`|`$decreasePostCount`|Whether to decrease the users' post counts
`bool`|`$ignoreRecycling`|Whether to ignore recycling board settings
`bool`|`$updateBoardCount`|Whether to adjust topic counts for the boards

Integration hooks
: integrate_remove_topics_before
: integrate_remove_topics

### removeMessage

```php
function removeMessage(int $message, bool $decreasePostCount = true): bool
```
Remove a specific message (including permission checks).



Type|Parameter|Description
---|---|---
`int`|`$message`|The message id
`bool`|`$decreasePostCount`|Whether to decrease users' post counts

Integration hooks
: integrate_pre_remove_message
: integrate_remove_message

### RestoreTopic

```php
function RestoreTopic(): void
```
Move back a topic from the recycle board to its original board.



### mergePosts

```php
function mergePosts(array $msgs, int $from_topic, int $target_topic): void
```
Take a load of messages from one place and stick them in a topic



Type|Parameter|Description
---|---|---
`array`|`$msgs`|The IDs of the posts to merge
`int`|`$from_topic`|The ID of the topic the messages were originally in
`int`|`$target_topic`|The ID of the topic the messages are being merged into

### removeDeleteConcurrence

```php
function removeDeleteConcurrence(): bool
```
Try to determine if the topic has already been deleted by another user.



