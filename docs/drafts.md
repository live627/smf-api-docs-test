---
layout: default
group: func
navtitle: Drafts.php
title: ./Sources/Drafts.php
count: 8
---
* auto-gen TOC:
{:toc}
### SaveDraft

```php
function SaveDraft(&$post_errors)
```
Saves a post draft in the user_drafts table
The core draft feature must be enabled, as well as the post draft option
Determines if this is a new or an existing draft
Returns errors in $post_errors for display in the template



Type|Parameter|Description
---|---|---
`string[]`|`$post_errors`|Any errors encountered trying to save this draft

### SavePMDraft

```php
function SavePMDraft(&$post_errors, $recipientList)
```
Saves a PM draft in the user_drafts table
The core draft feature must be enabled, as well as the pm draft option
Determines if this is a new or and update to an existing pm draft



Type|Parameter|Description
---|---|---
`string`|`$post_errors`|A string of info about errors encountered trying to save this draft
`array`|`$recipientList`|An array of data about who this PM is being sent to

### ReadDraft

```php
function ReadDraft($id_draft, $type = 0, $check = true, $load = false)
```
Reads a draft in from the user_drafts table
Validates that the draft is the user''s draft
Optionally loads the draft in to context or superglobal for loading in to the form



Type|Parameter|Description
---|---|---
`int`|`$id_draft`|ID of the draft to load
`int`|`$type`|Type of draft - 0 for post or 1 for PM
`bool`|`$check`|Validate that this draft belongs to the current user
`bool`|`$load`|Whether or not to load the data into variables for use on a form

### DeleteDraft

```php
function DeleteDraft($id_draft, $check = true)
```
Deletes one or many drafts from the DB
Validates the drafts are from the user
is supplied an array of drafts will attempt to remove all of them



Type|Parameter|Description
---|---|---
`int`|`$id_draft`|The ID of the draft to delete
`bool`|`$check`|Whether or not to check that the draft belongs to the current user

### ShowDrafts

```php
function ShowDrafts($member_id, $topic = false, $draft_type = 0)
```
Loads in a group of drafts for the user of a given type (0/posts, 1/pm's)
loads a specific draft for forum use if selected.

Used in the posting screens to allow draft selection
Will load a draft if selected is supplied via post

Type|Parameter|Description
---|---|---
`int`|`$member_id`|ID of the member to show drafts for
`bool&#124;int`|`$topic`|If $type is 1, this can be set to only load drafts for posts in the specific topic
`int`|`$draft_type`|The type of drafts to show - 0 for post drafts, 1 for PM drafts

### XmlDraft

```php
function XmlDraft($id_draft)
```
Returns an xml response to an autosave ajax request
provides the id of the draft saved and the time it was saved



Type|Parameter|Description
---|---|---
`int`|`$id_draft`|

### showProfileDrafts

```php
function showProfileDrafts($memID, $draft_type = 0)
```
Show all drafts of a given type by the current user
Uses the showdraft template
Allows for the deleting and loading/editing of drafts



Type|Parameter|Description
---|---|---
`int`|`$memID`|
`int`|`$draft_type`|

### showPMDrafts

```php
function showPMDrafts($memID = -1)
```
Show all PM drafts of the current user
Uses the showpmdraft template
Allows for the deleting and loading/editing of drafts



Type|Parameter|Description
---|---|---
`int`|`$memID`|

