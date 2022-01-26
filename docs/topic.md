---
layout: default
group: func
navtitle: Topic.php
title: ./Sources/Topic.php
count: 2
---
* auto-gen TOC:
{:toc}
### LockTopic

```php
function LockTopic(): void
```
Locks a topic... either by way of a moderator or the topic starter.

What this does:
- locks a topic, toggles between locked/unlocked/admin locked.
- only admins can unlock topics locked by other admins.
- requires the lock_own or lock_any permission.
- logs the action to the moderator log.
- returns to the topic after it is done.
- it is accessed via ?action=lock.

### Sticky

```php
function Sticky(): void
```
Sticky a topic.

Can't be done by topic starters - that would be annoying!
What this does:
 - stickies a topic - toggles between sticky and normal.
 - requires the make_sticky permission.
 - adds an entry to the moderator log.
 - when done, sends the user back to the topic.
 - accessed via ?action=sticky.

