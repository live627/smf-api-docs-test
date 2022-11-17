---
layout: default
group: func
navtitle: ManageMail.php
title: ./Sources/ManageMail.php
count: 9
---
* auto-gen TOC:
{:toc}
### ManageMail

```php
function ManageMail(): void
```
Main dispatcher. This function checks permissions and passes control through to the relevant section.



Integration hooks
: integrate_manage_mail

### BrowseMailQueue

```php
function BrowseMailQueue(): void
```
Display the mail queue.

..

### list_getMailQueue

```php
function list_getMailQueue(int $start, int $items_per_page, string $sort): array
```
This function grabs the mail queue items from the database, according to the params given.

Callback for $listOptions['get_items'] in BrowseMailQueue()

Type|Parameter|Description
---|---|---
`int`|`$start`|The item to start with \(for pagination purposes\)
`int`|`$items_per_page`|How many items to show on each page
`string`|`$sort`|A string indicating how to sort the results

### list_getMailQueueSize

```php
function list_getMailQueueSize(): int
```
Returns the total count of items in the mail queue.

Callback for $listOptions['get_count'] in BrowseMailQueue

### ModifyMailSettings

```php
function ModifyMailSettings(bool $return_config = false): void|array
```
Allows to view and modify the mail settings.



Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether to return the $config\_vars array \(used for admin search\)

Integration hooks
: integrate_modify_mail_settings
: integrate_save_mail_settings

### ClearMailQueue

```php
function ClearMailQueue(): void
```
This function clears the mail queue of all emails, and at the end redirects to browse.



### pauseMailQueueClear

```php
function pauseMailQueueClear(): void
```
Used for pausing the mail queue.



### TestMailSend

```php
function TestMailSend(): void
```
Test mail sending ability.



### time_since

```php
function time_since(int $time_diff): string
```
Little utility function to calculate how long ago a time was.



Type|Parameter|Description
---|---|---
`int`|`$time_diff`|The time difference, in seconds

