---
layout: default
group: func
navtitle: PostModeration.php
title: ./Sources/PostModeration.php
count: 9
---
* auto-gen TOC:
{:toc}
### PostModerationMain

```php
function PostModerationMain(): void
```
This is a handling function for all things post moderation.



### UnapprovedPosts

```php
function UnapprovedPosts(): void
```
View all unapproved posts.



### UnapprovedAttachments

```php
function UnapprovedAttachments(): void
```
View all unapproved attachments.



### list_getUnapprovedAttachments

```php
function list_getUnapprovedAttachments(int $start, int $items_per_page, string $sort, string $approve_query): array
```
Callback function for UnapprovedAttachments
retrieve all the attachments waiting for approval the approver can approve



Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with (for pagination purposes)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string indicating how to sort the results
`string`|`$approve_query`|Additional restrictions based on the boards the approver can see

### list_getNumUnapprovedAttachments

```php
function list_getNumUnapprovedAttachments(string $approve_query): int
```
Callback function for UnapprovedAttachments
count all the attachments waiting for approval that this approver can approve



Type|Parameter|Description
---|---|---
`string`|`$approve_query`|Additional restrictions based on the boards the approver can see

### ApproveMessage

```php
function ApproveMessage(): void
```
Approve a post, just the one.



### approveMessages

```php
function approveMessages(array $messages, array $messageDetails, string $current_view = 'replies'): void
```
Approve a batch of posts (or topics in their own right)



Type|Parameter|Description
---|---|---
`array`|`$messages`|The IDs of the messages to approve
`array`|`$messageDetails`|An array of information about each message, for the log
`string`|`$current_view`|What type of unapproved items we're approving - can be 'topics' or 'replies'

### approveAllData

```php
function approveAllData(): void
```
This is a helper function - basically approve everything!



### removeMessages

```php
function removeMessages(array $messages, array $messageDetails, string $current_view = 'replies'): void
```
Remove a batch of messages (or topics)



Type|Parameter|Description
---|---|---
`array`|`$messages`|The IDs of the messages to remove
`array`|`$messageDetails`|An array of information about the messages for the log
`string`|`$current_view`|What type of item we're removing - can be 'topics' or 'replies'

