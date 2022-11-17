---
layout: default
group: func
navtitle: Recent.php
title: ./Sources/Recent.php
count: 4
---
* auto-gen TOC:
{:toc}
### getLastPost

```php
function getLastPost(): array
```
Get the latest post made on the system

- respects approved, recycled, and board permissions

### RecentPosts

```php
function RecentPosts(): void
```
Find the ten most recent posts.



Integration hooks
: integrate_recent_RecentPosts

### getBoardParams

```php
function getBoardParams(): array
```
### UnreadTopics

```php
function UnreadTopics(): void
```
Find unread topics and replies.



Integration hooks
: integrate_recent_buttons
: integrate_unread_list

