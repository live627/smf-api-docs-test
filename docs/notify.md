---
layout: default
group: func
navtitle: Notify.php
title: ./Sources/Notify.php
count: 3
---
* auto-gen TOC:
{:toc}
### BoardNotify

```php
function BoardNotify(): void
```
Turn off/on notification for a particular board.

Must be called with a board specified in the URL.
Only uses the template if no mode (or subaction) was given.
Redirects the user back to the board after it is done.
Accessed via ?action=notifyboard.

### TopicNotify

```php
function TopicNotify(): void
```
Turn off/on unread replies subscription for a topic as well as sets individual topic's alert preferences
Must be called with a topic specified in the URL.

The mode can be from 0 to 3
0 => unwatched, 1 => no alerts/emails, 2 => alerts, 3 => emails/alerts
Upon successful completion of action will direct user back to topic.
Accessed via ?action=notifytopic.

### AnnouncementsNotify

```php
function AnnouncementsNotify(): void
```
Turn off/on notifications for announcements.

Only uses the template if no mode was given.
Accessed via ?action=notifyannouncements.

