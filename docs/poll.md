---
layout: default
group: func
navtitle: Poll.php
title: ./Sources/Poll.php
count: 5
---
* auto-gen TOC:
{:toc}
### Vote

```php
function Vote()
```
Allow the user to vote.

It is called to register a vote in a poll.
Must be called with a topic and option specified.
Requires the poll_vote permission.
Upon successful completion of action will direct user back to topic.
Accessed via ?action=vote.

Uses Post language file.

### LockVoting

```php
function LockVoting()
```
Lock the voting for a poll.

Must be called with a topic specified in the URL.
An admin always has over riding permission to lock a poll.
If not an admin must have poll_lock_any permission, otherwise must
be poll starter with poll_lock_own permission.
Upon successful completion of action will direct user back to topic.
Accessed via ?action=lockvoting.

### EditPoll

```php
function EditPoll()
```
Display screen for editing or adding a poll.

Must be called with a topic specified in the URL.
If the user is adding a poll to a topic, must contain the variable
'add' in the url.
User must have poll_edit_any/poll_add_any permission for the
relevant action, otherwise must be poll starter with poll_edit_own
permission for editing, or be topic starter with poll_add_any permission for adding.
Accessed via ?action=editpoll.

Uses Post language file.
Uses Poll template, main sub-template.

### EditPoll2

```php
function EditPoll2()
```
Update the settings for a poll, or add a new one.

Must be called with a topic specified in the URL.
The user must have poll_edit_any/poll_add_any permission
for the relevant action. Otherwise they must be poll starter
with poll_edit_own permission for editing, or be topic starter
with poll_add_any permission for adding.
In the case of an error, this function will redirect back to
EditPoll and display the relevant error message.
Upon successful completion of action will direct user back to topic.
Accessed via ?action=editpoll2.

### RemovePoll

```php
function RemovePoll()
```
Remove a poll from a topic without removing the topic.

Must be called with a topic specified in the URL.
Requires poll_remove_any permission, unless it's the poll starter
with poll_remove_own permission.
Upon successful completion of action will direct user back to topic.
Accessed via ?action=removepoll.

