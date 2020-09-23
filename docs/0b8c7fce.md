---
layout: default
title: ManageErrors.php
count: 4
---

# ./Sources/ManageErrors.php

### ViewErrorLog

```php
function ViewErrorLog()
```
View the forum's error log.

This function sets all the context up to show the error log for maintenance.
It requires the maintain_forum permission.
It is accessed from ?action=admin;area=logs;sa=errorlog.


### deleteErrors

```php
function deleteErrors()
```
Delete all or some of the errors in the error log.

It applies any necessary filters to deletion.
This should only be called by ViewErrorLog().
It attempts to TRUNCATE the table to reset the auto_increment.
Redirects back to the error log when done.


### ViewFile

```php
function ViewFile()
```
View a file specified in $_REQUEST['file'], with php highlighting on it
Preconditions:
 - file must be readable,
 - full file path must be base64 encoded,
 - user must have admin_forum permission.

The line number number is specified by $_REQUEST['line']...
The function will try to get the 20 lines before and after the specified line.


### ViewBacktrace

```php
function ViewBacktrace()
```
View a backtrace specified in $_REQUEST['backtrace'], with php highlighting on it
Preconditions:
 - user must have admin_forum permission.




