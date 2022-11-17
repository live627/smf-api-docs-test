---
layout: default
group: func
navtitle: Who.php
title: ./Sources/Who.php
count: 3
---
* auto-gen TOC:
{:toc}
### Who

```php
function Who(): void
```
Who's online, and what are they doing?
This function prepares the who's online data for the Who template.

It requires the who_view permission.
It is enabled with the who_enabled setting.
It is accessed via ?action=who.

Uses Who template, main sub-template
Uses Who language file.

### determineActions

```php
function determineActions(mixed $urls, string|bool $preferred_prefix = false): array
```
This function determines the actions of the members passed in urls.

Adding actions to the Who's Online list:
Adding actions to this list is actually relatively easy...
 - for actions anyone should be able to see, just add a string named whoall_ACTION.
   (where ACTION is the action used in index.php.)
 - for actions that have a subaction which should be represented differently, use whoall_ACTION_SUBACTION.
 - for actions that include a topic, and should be restricted, use whotopic_ACTION.
 - for actions that use a message, by msg or quote, use whopost_ACTION.
 - for administrator-only actions, use whoadmin_ACTION.
 - for actions that should be viewable only with certain permissions,
   use whoallow_ACTION and add a list of possible permissions to the
   $allowedActions array, using ACTION as the key.

Type|Parameter|Description
---|---|---
`mixed`|`$urls`|a single url \(string\) or an array of arrays, each inner array being \(JSON\-encoded request data, id\_member\)
`string` &#124; `bool`|`$preferred_prefix`|= false

Integration hooks
: who_allowed
: integrate_whos_online
: whos_online_after

### Credits

```php
function Credits(bool $in_admin = false): void
```
It prepares credit and copyright information for the credits page or the admin page



Type|Parameter|Description
---|---|---
`bool`|`$in_admin`|= false, if parameter is true the it will not load the sub\-template nor the template file

Integration hooks
: integrate_credits

