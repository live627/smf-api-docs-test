---
layout: default
navtitle: RepairBoards.php
title: ./Sources/RepairBoards.php
count: 5
---

### RepairBoards

```php
function RepairBoards()
```
Finds or repairs errors in the database to fix possible problems.

Requires the admin_forum permission.
Calls createSalvageArea() to create a new board, if necessary.
Accessed by ?action=admin;area=repairboards.

### pauseRepairProcess

```php
function pauseRepairProcess($to_fix, $current_step_description, $max_substep = 0, $force = false)
```
Show the not_done template to avoid CGI timeouts and similar.

Called when 3 or more seconds have passed while searching for errors.
If max_substep is set, $_GET['substep'] / $max_substep is the percent
done this step is.

Type|Parameter|Description
---|---|---
`php array`|`php $to_fix`|An array of information about what to fix
`php string`|`php $current_step_description`|The description of the current step
`php int`|`php $max_substep`|The maximum substep to reach before pausing
`php bool`|`php $force`|Whether to force pausing even if we don't really need to

### loadForumTests

```php
function loadForumTests()
```
Load up all the tests we might want to do ;)



### findForumErrors

```php
function findForumErrors($do_fix = false)
```
Checks for errors in steps, until 5 seconds have passed.

It keeps track of the errors it did find, so that the actual repair
won't have to recheck everything.

Type|Parameter|Description
---|---|---
`php bool`|`php $do_fix`|Whether to actually fix the errors or just return the info

### createSalvageArea

```php
function createSalvageArea()
```
Create a salvage area for repair purposes, if one doesn't already exist.

Uses the forum's default language, and checks based on that name.

