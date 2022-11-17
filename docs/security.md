---
layout: default
group: func
navtitle: Security.php
title: ./Sources/Security.php
count: 20
---
* auto-gen TOC:
{:toc}
### validateSession

```php
function validateSession(string $type = 'admin', string $force = false): void|string
```
Check if the user is who he/she says he is
Makes sure the user is who they claim to be by requiring a password to be typed in every hour.

Is turned on and off by the securityDisable setting.
Uses the adminLogin() function of Subs-Auth.php if they need to login, which saves all request (post and get) data.

Type|Parameter|Description
---|---|---
`string`|`$type`|What type of session this is
`string`|`$force`|When true, require a password even if we normally wouldn't

Integration hooks
: integrate_validateSession
: integrate_verify_password

### is_not_guest

```php
function is_not_guest(string $message = ''): void
```
Require a user who is logged in. (not a guest.)
Checks if the user is currently a guest, and if so asks them to login with a message telling them why.

Message is what to tell them when asking them to login.

Type|Parameter|Description
---|---|---
`string`|`$message`|The message to display to the guest

### is_not_banned

```php
function is_not_banned(bool $forceCheck = false): void
```
Do banning related stuff.  (ie. disallow access....)
Checks if the user is banned, and if so dies with an error.

Caches this information for optimization purposes.

Type|Parameter|Description
---|---|---
`bool`|`$forceCheck`|Whether to force a recheck

### banPermissions

```php
function banPermissions(): void
```
Fix permissions according to ban status.

Applies any states of banning by removing permissions the user cannot have.

Integration hooks
: integrate_post_ban_permissions
: integrate_warn_permissions

### log_ban

```php
function log_ban(array $ban_ids = array(), string $email = null): void
```
Log a ban in the database.

Log the current user in the ban logs.
Increment the hit counters for the specified ban ID's (if any.)

Type|Parameter|Description
---|---|---
`array`|`$ban_ids`|The IDs of the bans
`string`|`$email`|The email address associated with the user that triggered this hit

### isBannedEmail

```php
function isBannedEmail(string $email, string $restriction, string $error): void
```
Checks if a given email address might be banned.

Check if a given email is banned.
Performs an immediate ban if the turns turns out positive.

Type|Parameter|Description
---|---|---
`string`|`$email`|The email to check
`string`|`$restriction`|What type of restriction (cannot_post, cannot_register, etc.)
`string`|`$error`|The error message to display if they are indeed banned

### checkSession

```php
function checkSession(string $type = 'post', string $from_action = '', bool $is_fatal = true): string
```
Make sure the user's correct session was passed, and they came from here.

Checks the current session, verifying that the person is who he or she should be.
Also checks the referrer to make sure they didn't get sent here.
Depends on the disableCheckUA setting, which is usually missing.
Will check GET, POST, or REQUEST depending on the passed type.
Also optionally checks the referring action if passed. (note that the referring action must be by GET.)

Type|Parameter|Description
---|---|---
`string`|`$type`|The type of check (post, get, request)
`string`|`$from_action`|The action this is coming from
`bool`|`$is_fatal`|Whether to die with a fatal error if the check fails

### checkConfirm

```php
function checkConfirm(string $action): bool|string
```
Check if a specific confirm parameter was given.



Type|Parameter|Description
---|---|---
`string`|`$action`|The action we want to check against

### createToken

```php
function createToken(string $action, string $type = 'post'): array
```
Lets give you a token of our appreciation.



Type|Parameter|Description
---|---|---
`string`|`$action`|The action to create the token for
`string`|`$type`|The type of token ('post', 'get' or 'request')

### validateToken

```php
function validateToken(string $action, string $type = 'post', bool $reset = true): bool
```
Only patrons with valid tokens can ride this ride.



Type|Parameter|Description
---|---|---
`string`|`$action`|The action to validate the token for
`string`|`$type`|The type of request (get, request, or post)
`bool`|`$reset`|Whether to reset the token and display an error if validation fails

### cleanTokens

```php
function cleanTokens(bool $complete = false): void
```
Removes old unused tokens from session
defaults to 3 hours before a token is considered expired
if $complete = true will remove all tokens



Type|Parameter|Description
---|---|---
`bool`|`$complete`|Whether to remove all tokens or only expired ones

### checkSubmitOnce

```php
function checkSubmitOnce(string $action, bool $is_fatal = true): void|bool
```
Check whether a form has been submitted twice.

Registers a sequence number for a form.
Checks whether a submitted sequence number is registered in the current session.
Depending on the value of is_fatal shows an error or returns true or false.
Frees a sequence number from the stack after it's been checked.
Frees a sequence number without checking if action == 'free'.

Type|Parameter|Description
---|---|---
`string`|`$action`|The action - can be 'register', 'check' or 'free'
`bool`|`$is_fatal`|Whether to die with a fatal error

### allowedTo

```php
function allowedTo(string|array $permission, int|array $boards = null, bool $any = false): bool
```
Check the user's permissions.

checks whether the user is allowed to do permission. (ie. post_new.)
If boards is specified, checks those boards instead of the current one.
If any is true, will return true if the user has the permission on any of the specified boards
Always returns true if the user is an administrator.

Type|Parameter|Description
---|---|---
`string`&#124;`array`|`$permission`|A single permission to check or an array of permissions to check
`int`&#124;`array`|`$boards`|The ID of a board or an array of board IDs if we want to check board-level permissions
`bool`|`$any`|Whether to check for permission on at least one board instead of all boards

Integration hooks
: integrate_allowed_to_general
: integrate_allowed_to_board

### isAllowedTo

```php
function isAllowedTo(string|array $permission, int|array $boards = null, bool $any = false): void
```
Fatal error if they cannot.

Uses allowedTo() to check if the user is allowed to do permission.
Checks the passed boards or current board for the permission.
If $any is true, the user only needs permission on at least one of the boards to pass
If they are not, it loads the Errors language file and shows an error using $txt['cannot_' . $permission].
If they are a guest and cannot do it, this calls is_not_guest().

Type|Parameter|Description
---|---|---
`string`&#124;`array`|`$permission`|A single permission to check or an array of permissions to check
`int`&#124;`array`|`$boards`|The ID of a single board or an array of board IDs if we're checking board-level permissions (null otherwise)
`bool`|`$any`|Whether to check for permission on at least one board instead of all boards

Integration hooks
: integrate_heavy_permissions_session

### boardsAllowedTo

```php
function boardsAllowedTo(string|array $permissions, bool $check_access = true, bool $simple = true): array
```
Return the boards a user has a certain (board) permission on. (array(0) if all.)
 - returns a list of boards on which the user is allowed to do the specified permission.

- returns an array with only a 0 in it if the user has permission to do this on every board.
 - returns an empty array if he or she cannot do this on any board.
If check_access is true will also make sure the group has proper access to that board.

Type|Parameter|Description
---|---|---
`string`&#124;`array`|`$permissions`|A single permission to check or an array of permissions to check
`bool`|`$check_access`|Whether to check only the boards the user has access to
`bool`|`$simple`|Whether to return a simple array of board IDs or one with permissions as the keys

Integration hooks
: integrate_boards_allowed_to

### spamProtection

```php
function spamProtection(string $error_type, bool $only_return_result = true): bool
```
This function attempts to protect from spammed messages and the like.

The time taken depends on error_type - generally uses the modSetting.

Type|Parameter|Description
---|---|---
`string`|`$error_type`|The error type. Also used as a $txt index (not an actual string).
`bool`|`$only_return_result`|Whether you want the function to die with a fatal_lang_error.

Integration hooks
: integrate_spam_protection

### secureDirectory

```php
function secureDirectory(string|array $paths, bool $attachments = false): bool|array
```
A generic function to create a pair of index.php and .htaccess files in a directory



Type|Parameter|Description
---|---|---
`string`&#124;`array`|`$paths`|The (absolute) directory path
`bool`|`$attachments`|Whether this is an attachment directory

### frameOptionsHeader

```php
function frameOptionsHeader(string $override = null): void
```
This sets the X-Frame-Options header.



Type|Parameter|Description
---|---|---
`string`|`$override`|An option to override (either 'SAMEORIGIN' or 'DENY')

### get_allowed_http_origin

```php
/*
 * Determines if the HTTP origin is an authorized one.
 *
 * @param string $origin
 *
 * @since 2.1
 */
function get_allowed_http_origin($origin)
```
### corsPolicyHeader

```php
function corsPolicyHeader(bool $set_header = true): void
```
This sets the Access-Control-Allow-Origin header.



Type|Parameter|Description
---|---|---
`bool`|`$set_header`|(Default: true): When false, we will do the logic, but not send the headers.  The relevant logic is still saved in the $context and can be sent manually.

