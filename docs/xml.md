---
layout: default
group: func
navtitle: Xml.php
title: ./Sources/Xml.php
count: 8
---
* auto-gen TOC:
{:toc}
### XMLhttpMain

```php
function XMLhttpMain(): void
```
The main handler and designator for AJAX stuff - jumpto, message icons and previews



### GetJumpTo

```php
function GetJumpTo(): void
```
Get a list of boards and categories used for the jumpto dropdown.



### ListMessageIcons

```php
function ListMessageIcons(): void
```
Gets a list of available message icons and sends the info to the template for display



### RetrievePreview

```php
function RetrievePreview(): void|bool
```
Handles retrieving previews of news items, newsletters, signatures and warnings.

Calls the appropriate function based on $_POST['item']

### newspreview

```php
function newspreview(): void
```
Handles previewing news items



### newsletterpreview

```php
function newsletterpreview(): void
```
Handles previewing newsletters



### sig_preview

```php
function sig_preview(): void
```
Handles previewing signatures



### warning_preview

```php
function warning_preview(): void
```
Handles previewing user warnings



