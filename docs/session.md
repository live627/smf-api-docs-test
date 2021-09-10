---
layout: default
group: func
navtitle: Session.php
title: ./Sources/Session.php
count: 7
---
* auto-gen TOC:
{:toc}
### loadSession

```php
function loadSession()
```
Attempt to start the session, unless it already has been.



### sessionOpen

```php
function sessionOpen($save_path, $session_name)
```
Implementation of sessionOpen() replacing the standard open handler.

It simply returns true.

Type|Parameter|Description
---|---|---
`string`|`$save_path`|The path to save the session to
`string`|`$session_name`|The name of the session

### sessionClose

```php
function sessionClose()
```
Implementation of sessionClose() replacing the standard close handler.

It simply returns true.

### sessionRead

```php
function sessionRead($session_id)
```
Implementation of sessionRead() replacing the standard read handler.



Type|Parameter|Description
---|---|---
`string`|`$session_id`|The session ID

### sessionWrite

```php
function sessionWrite($session_id, $data)
```
Implementation of sessionWrite() replacing the standard write handler.



Type|Parameter|Description
---|---|---
`string`|`$session_id`|The session ID
`string`|`$data`|The data to write to the session

### sessionDestroy

```php
function sessionDestroy($session_id)
```
Implementation of sessionDestroy() replacing the standard destroy handler.



Type|Parameter|Description
---|---|---
`string`|`$session_id`|The session ID

### sessionGC

```php
function sessionGC($max_lifetime)
```
Implementation of sessionGC() replacing the standard gc handler.

Callback for garbage collection.

Type|Parameter|Description
---|---|---
`int`|`$max_lifetime`|The maximum lifetime (in seconds) - prevents deleting of sessions older than this

