---
layout: default
group: func
navtitle: PersonalMessage.php
title: ./Sources/PersonalMessage.php
count: 23
---
* auto-gen TOC:
{:toc}
### MessageMain

```php
function MessageMain(): void
```
This helps organize things.

..

### messageIndexBar

```php
function messageIndexBar(string $area): void
```
A menu to easily access different areas of the PM section



Type|Parameter|Description
---|---|---
`string`|`$area`|The area we're currently in

### MessagePopup

```php
function MessagePopup(): void
```
The popup for when we ask for the popup from the user.



### MessageFolder

```php
function MessageFolder(): void
```
A folder, ie. inbox/sent etc.



Integration hooks
: integrate_conversation_buttons

### prepareMessageContext

```php
function prepareMessageContext(string $type = 'subject', bool $reset = false): bool|array
```
Get a personal message for the theme.  (used to save memory.)



Type|Parameter|Description
---|---|---
`string`|`$type`|The type of message
`bool`|`$reset`|Whether to reset the internal pointer

Integration hooks
: integrate_prepare_pm_context

### MessageSearch

```php
function MessageSearch(): void
```
Allows searching through personal messages.



### MessageSearch2

```php
function MessageSearch2(): void
```
Actually do the search of personal messages.



Integration hooks
: integrate_search_pm_context

### MessagePost

```php
function MessagePost(): void
```
Send a new message?



Integration hooks
: integrate_pm_post

### MessageDrafts

```php
function MessageDrafts(): void
```
This function allows the user to view their PM drafts



### messagePostError

```php
function messagePostError(array $error_types, array $named_recipients, ??? $recipient_ids = array()): void
```
An error in the message.

..

Type|Parameter|Description
---|---|---
`array`|`$error_types`|An array of strings indicating which type of errors occurred
`array`|`$named_recipients`|
`null`|`$recipient_ids`|

Integration hooks
: integrate_pm_error

### MessagePost2

```php
function MessagePost2(): void
```
Send it!



### MessageActionsApply

```php
function MessageActionsApply(): void
```
This function performs all additional stuff.

..

### MessageKillAll

```php
function MessageKillAll(): void
```
Delete ALL the messages!



### MessagePrune

```php
function MessagePrune(): void
```
This function allows the user to delete all messages older than so many days.



### deleteMessages

```php
function deleteMessages(?array $personal_messages, ?string $folder = null, array|int|null $owner = null): void
```
Delete the specified personal messages.



Type|Parameter|Description
---|---|---
`array`&#124;`null`|`$personal_messages`|An array containing the IDs of PMs to delete or null to delete all of them
`string`&#124;`null`|`$folder`|Which "folder" to delete PMs from \- 'sent' to delete them from the outbox, null or anything else to delete from the inbox
`array`&#124;`int`&#124;`null`|`$owner`|An array of IDs of users whose PMs are being deleted, the ID of a single user or null to use the current user's ID

### markMessages

```php
function markMessages(?array $personal_messages = null, ?int $label = null, ?int $owner = null): void
```
Mark the specified personal messages read.



Type|Parameter|Description
---|---|---
`array`&#124;`null`|`$personal_messages`|An array of PM IDs to mark or null to mark all
`int`&#124;`null`|`$label`|The ID of a label\. If set, only messages with this label will be marked\.
`int`&#124;`null`|`$owner`|If owner is set, marks messages owned by that member id

### ManageLabels

```php
function ManageLabels(): void
```
This function handles adding, deleting and editing labels on messages.



### MessageSettings

```php
function MessageSettings(): void
```
Allows to edit Personal Message Settings.

Uses Profile.php
Uses Profile-Modify.php
Uses Profile template.
Uses Profile language file.

### ReportMessage

```php
function ReportMessage(): void
```
Allows the user to report a personal message to an administrator.

- In the first instance requires that the ID of the message to report is passed through $_GET.
- It allows the user to report to either a particular administrator - or the whole admin team.
- It will forward on a copy of the original message without allowing the reporter to make changes.

### ManageRules

```php
function ManageRules(): void
```
List all rules, and allow adding/entering etc.

..

### ApplyRules

```php
function ApplyRules(bool $all_messages = false): void
```
This will apply rules to all unread messages. If all_messages is set will, clearly, do it to all!



Type|Parameter|Description
---|---|---
`bool`|`$all_messages`|Whether to apply this to all messages or just unread ones

### LoadRules

```php
function LoadRules(bool $reload = false): void
```
Load up all the rules for the current user.



Type|Parameter|Description
---|---|---
`bool`|`$reload`|Whether or not to reload all the rules from the database if $context\['rules'\] is set

### isAccessiblePM

```php
function isAccessiblePM(int $pmID, string $validFor = 'in_or_outbox'): bool
```
Check if the PM is available to the current user.



Type|Parameter|Description
---|---|---
`int`|`$pmID`|The ID of the PM
`string`|`$validFor`|Which folders this is valud for \- can be 'inbox', 'outbox' or 'in\_or\_outbox'

