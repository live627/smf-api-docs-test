---
layout: default
group: func
navtitle: SplitTopics.php
title: ./Sources/SplitTopics.php
count: 10
---
* auto-gen TOC:
{:toc}
### SplitTopics

```php
function SplitTopics(): void
```
splits a topic into two topics.

delegates to the other functions (based on the URL parameter 'sa').
loads the SplitTopics template.
requires the split_any permission.
is accessed with ?action=splittopics.

### SplitIndex

```php
function SplitIndex(): void
```
screen shown before the actual split.

is accessed with ?action=splittopics;sa=index.
default sub action for ?action=splittopics.
uses 'ask' sub template of the SplitTopics template.
redirects to SplitSelectTopics if the message given turns out to be
the first message of a topic.
shows the user three ways to split the current topic.

### SplitExecute

```php
function SplitExecute(): void
```
do the actual split.

is accessed with ?action=splittopics;sa=execute.
uses the main SplitTopics template.
supports three ways of splitting:
(1) only one message is split off.
(2) all messages after and including a given message are split off.
(3) select topics to split (redirects to SplitSelectTopics()).
uses splitTopic function to do the actual splitting.

### SplitSelectTopics

```php
function SplitSelectTopics(): void
```
allows the user to select the messages to be split.

is accessed with ?action=splittopics;sa=selectTopics.
uses 'select' sub template of the SplitTopics template or (for
XMLhttp) the 'split' sub template of the Xml template.
supports XMLhttp for adding/removing a message to the selection.
uses a session variable to store the selected topics.
shows two independent page indexes for both the selected and
not-selected messages (;topic=1.x;start2=y).

### SplitSelectionExecute

```php
function SplitSelectionExecute(): void
```
do the actual split of a selection of topics.

is accessed with ?action=splittopics;sa=splitSelection.
uses the main SplitTopics template.
uses splitTopic function to do the actual splitting.

### splitTopic

```php
function splitTopic(int $split1_ID_TOPIC, array $splitMessages, string $new_subject): int
```
general function to split off a topic.

creates a new topic and moves the messages with the IDs in
array messagesToBeSplit to the new topic.
the subject of the newly created topic is set to 'newSubject'.
marks the newly created message as read for the user splitting it.
updates the statistics to reflect a newly created topic.
logs the action in the moderation log.
a notification is sent to all users monitoring this topic.

Type|Parameter|Description
---|---|---
`int`|`$split1_ID_TOPIC`|The ID of the topic we're splitting
`array`|`$splitMessages`|The IDs of the messages being split
`string`|`$new_subject`|The subject of the new topic

### MergeTopics

```php
function MergeTopics(): void
```
merges two or more topics into one topic.

delegates to the other functions (based on the URL parameter sa).
loads the SplitTopics template.
requires the merge_any permission.
is accessed with ?action=mergetopics.

### MergeIndex

```php
function MergeIndex(): void
```
allows to pick a topic to merge the current topic with.

is accessed with ?action=mergetopics;sa=index
default sub action for ?action=mergetopics.
uses 'merge' sub template of the MoveTopic template.
allows to set a different target board.

### MergeExecute

```php
function MergeExecute(array $topics = array()): void
```
set merge options and do the actual merge of two or more topics.

the merge options screen:
* shows topics to be merged and allows to set some merge options.
* is accessed by ?action=mergetopics;sa=options.and can also internally be called by QuickModeration() (Subs-Boards.php).
* uses 'merge_extra_options' sub template of the MoveTopic template.

the actual merge:
* is accessed with ?action=mergetopics;sa=execute.
* updates the statistics to reflect the merge.
* logs the action in the moderation log.
* sends a notification is sent to all users monitoring this topic.
* redirects to ?action=mergetopics;sa=done.

Type|Parameter|Description
---|---|---
`array`|`$topics`|The IDs of the topics to merge

### MergeDone

```php
function MergeDone(): void
```
Shows a 'merge completed' screen.

is accessed with ?action=mergetopics;sa=done.
uses 'merge_done' sub template of the SplitTopics template.

