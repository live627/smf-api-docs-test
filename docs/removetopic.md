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
function RemoveTopic2()
```
Completely remove an entire topic.

Redirects to the board when completed.

### DeleteMessage

```php
function DeleteMessage()
```
Remove just a single post.

On completion redirect to the topic or to the board.

### RemoveOldTopics2

```php
function RemoveOldTopics2()
```
So long as you are sure... all old posts will be gone.

Used in ManageMaintenance.php to prune old topics.

### removeTopics

```php
function removeTopics($topics, $decreasePostCount = true, $ignoreRecycling = false, $updateBoardCount = true)
```
Removes the passed id_topic's. (permissions are NOT checked here!).



Type|Parameter|Description
---|---|---
`array&#124;int`|`$topics`|The topics to remove (can be an id or an array of ids).
`bool`|`$decreasePostCount`|Whether to decrease the users' post counts
`bool`|`$ignoreRecycling`|Whether to ignore recycling board settings
`bool`|`$updateBoardCount`|Whether to adjust topic counts for the boards

### removeMessage

```php
function removeMessage($message, $decreasePostCount = true)
```
Remove a specific message (including permission checks).



Type|Parameter|Description
---|---|---
`int`|`$message`|The message id
`bool`|`$decreasePostCount`|Whether to decrease users' post counts

### RestoreTopic

```php
function RestoreTopic()
```
Move back a topic from the recycle board to its original board.



### mergePosts

```php
function mergePosts($msgs, $from_topic, $target_topic)
```
Take a load of messages from one place and stick them in a topic



Type|Parameter|Description
---|---|---
`array`|`$msgs`|The IDs of the posts to merge
`int`|`$from_topic`|The ID of the topic the messages were originally in
`int`|`$target_topic`|The ID of the topic the messages are being merged into

### removeDeleteConcurrence

```php
function removeDeleteConcurrence()
```
Try to determine if the topic has already been deleted by another user.



