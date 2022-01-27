---
layout: default
group: func
navtitle: ManageMembers.php
title: ./Sources/ManageMembers.php
count: 7
---
* auto-gen TOC:
{:toc}
### ViewMembers

```php
function ViewMembers(): void
```
The main entrance point for the Manage Members screen.

As everyone else, it calls a function based on the given sub-action.
Called by ?action=admin;area=viewmembers.
Requires the moderate_forum permission.

Uses ManageMembers template
Uses ManageMembers language file.

Integration hooks
: integrate_manage_members

### ViewMemberlist

```php
function ViewMemberlist(): void
```
View all members list. It allows sorting on several columns, and deletion of
selected members. It also handles the search query sent by
?action=admin;area=viewmembers;sa=search.

Called by ?action=admin;area=viewmembers;sa=all or ?action=admin;area=viewmembers;sa=query.
Requires the moderate_forum permission.

Uses a standard list (@see createList())

Integration hooks
: integrate_view_members_params

### SearchMembers

```php
function SearchMembers(): void
```
Search the member list, using one or more criteria.

Called by ?action=admin;area=viewmembers;sa=search.
Requires the moderate_forum permission.
form is submitted to action=admin;area=viewmembers;sa=query.

### MembersAwaitingActivation

```php
function MembersAwaitingActivation(): void
```
List all members who are awaiting approval / activation, sortable on different columns.

It allows instant approval or activation of (a selection of) members.
Called by ?action=admin;area=viewmembers;sa=browse;type=approve
 or ?action=admin;area=viewmembers;sa=browse;type=activate.
The form submits to ?action=admin;area=viewmembers;sa=approve.
Requires the moderate_forum permission.

### AdminApprove

```php
function AdminApprove(): void
```
This function handles the approval, rejection, activation or deletion of members.

Called by ?action=admin;area=viewmembers;sa=approve.
Requires the moderate_forum permission.
Redirects to ?action=admin;area=viewmembers;sa=browse
with the same parameters as the calling page.

Integration hooks
: integrate_activate

### jeffsdatediff

```php
function jeffsdatediff(int $old): int
```
Nifty function to calculate the number of days ago a given date was.

Requires a unix timestamp as input, returns an integer.
Named in honour of Jeff Lewis, the original creator of...this function.

Type|Parameter|Description
---|---|---
`int`|`$old`|The timestamp of the old date

### GetMemberActivationCounts

```php
function GetMemberActivationCounts(): void
```
Fetches all the activation counts for ViewMembers.



