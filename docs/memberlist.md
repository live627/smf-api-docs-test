---
layout: default
group: func
navtitle: Memberlist.php
title: ./Sources/Memberlist.php
count: 5
---
* auto-gen TOC:
{:toc}
### Memberlist

```php
function Memberlist(): void
```
Shows a listing of registered members.

- If a subaction is not specified, lists all registered members.
- It allows searching for members with the 'search' sub action.
- It calls MLAll or MLSearch depending on the sub action.
- Requires the view_mlist permission.
- Accessed via ?action=mlist.

Uses Memberlist template, main sub template.

Integration hooks
: integrate_memberlist_buttons

### MLAll

```php
function MLAll(): void
```
List all members, page by page, with sorting.

Called from MemberList().
Can be passed a sort parameter, to order the display of members.
Calls printMemberListRows to retrieve the results of the query.

### MLSearch

```php
function MLSearch(): void
```
Search for members, or display search results.

- Called by MemberList().
- If variable 'search' is empty displays search dialog box, using the search sub template.
- Calls printMemberListRows to retrieve the results of the query.

### printMemberListRows

```php
function printMemberListRows(resource $request): void
```
Retrieves results of the request passed to it
Puts results of request into the context for the sub template.



Type|Parameter|Description
---|---|---
`resource`|`$request`|An SQL result resource

### getCustFieldsMList

```php
function getCustFieldsMList(): array
```
Sets the label, sort and join info for every custom field column.



