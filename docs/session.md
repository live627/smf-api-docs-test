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
function loadSession(): void
```
Attempt to start the session, unless it already has been.



Integration hooks
: integrate_load_session
: integrate_session_handlers

### sessionOpen

```php
function sessionOpen(string $save_path, string $session_name): bool
```
Implementation of sessionOpen() replacing the standard open handler.

It simply returns true.

Type|Parameter|Description
---|---|---
`string`|`$save_path`|The path to save the session to
`string`|`$session_name`|The name of the session

### sessionClose

```php
function sessionClose(): bool
```
Implementation of sessionClose() replacing the standard close handler.

It simply returns true.

### sessionRead

```php
function sessionRead(string $session_id): string
```
Implementation of sessionRead() replacing the standard read handler.



Type|Parameter|Description
---|---|---
`string`|`$session_id`|The session ID

### sessionWrite

```php
function sessionWrite(string $session_id, string $data): bool
```
Implementation of sessionWrite() replacing the standard write handler.



Type|Parameter|Description
---|---|---
`string`|`$session_id`|The session ID
`string`|`$data`|The data to write to the session

### sessionDestroy

```php
function sessionDestroy(string $session_id): bool
```
Implementation of sessionDestroy() replacing the standard destroy handler.



Type|Parameter|Description
---|---|---
`string`|`$session_id`|The session ID

### sessionGC

```php
function sessionGC(int $max_lifetime): bool
```
Implementation of sessionGC() replacing the standard gc handler.

Callback for garbage collection.

Type|Parameter|Description
---|---|---
`int`|`$max_lifetime`|The maximum lifetime \(in seconds\) \- prevents deleting of sessions older than this

