---
layout: default
group: func
navtitle: Security.php
title: ./Sources/Security.php
count: 22
---
* auto-gen TOC:
{:toc}
### validateSession

```php
function validateSession($type = 'admin', $force = false)
```
Check if the user is who he/she says he is
Makes sure the user is who they claim to be by requiring a password to be typed in every hour.

Is turned on and off by the securityDisable setting.
Uses the adminLogin() function of Subs-Auth.php if they need to login, which saves all request (post and get) data.

Type|Parameter|Description
---|---|---
`string`|`$type`|What type of session this is
`string`|`$force`|When true, require a password even if we normally wouldn't

### is_not_guest

```php
function is_not_guest($message = '')
```
Require a user who is logged in. (not a guest.)
Checks if the user is currently a guest, and if so asks them to login with a message telling them why.

Message is what to tell them when asking them to login.

Type|Parameter|Description
---|---|---
`string`|`$message`|The message to display to the guest

### is_not_banned

```php
function is_not_banned($forceCheck = false)
```
Do banning related stuff.  (ie. disallow access....)
Checks if the user is banned, and if so dies with an error.

Caches this information for optimization purposes.

Type|Parameter|Description
---|---|---
`bool`|`$forceCheck`|Whether to force a recheck

### banPermissions

```php
function banPermissions()
```
Fix permissions according to ban status.

Applies any states of banning by removing permissions the user cannot have.

### log_ban

```php
function log_ban($ban_ids = array(), $email = null)
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
function isBannedEmail($email, $restriction, $error)
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
function checkSession($type = 'post', $from_action = '', $is_fatal = true)
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
function checkConfirm($action)
```
Check if a specific confirm parameter was given.



Type|Parameter|Description
---|---|---
`string`|`$action`|The action we want to check against

### createToken

```php
function createToken($action, $type = 'post')
```
Lets give you a token of our appreciation.



Type|Parameter|Description
---|---|---
`string`|`$action`|The action to create the token for
`string`|`$type`|The type of token ('post', 'get' or 'request')

### validateToken

```php
function validateToken($action, $type = 'post', $reset = true)
```
Only patrons with valid tokens can ride this ride.



Type|Parameter|Description
---|---|---
`string`|`$action`|The action to validate the token for
`string`|`$type`|The type of request (get, request, or post)
`bool`|`$reset`|Whether to reset the token and display an error if validation fails

### cleanTokens

```php
function cleanTokens($complete = false)
```
Removes old unused tokens from session
defaults to 3 hours before a token is considered expired
if $complete = true will remove all tokens



Type|Parameter|Description
---|---|---
`bool`|`$complete`|Whether to remove all tokens or only expired ones

### checkSubmitOnce

```php
function checkSubmitOnce($action, $is_fatal = true)
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
function allowedTo($permission, $boards = null, $any = false)
```
Check the user's permissions.

checks whether the user is allowed to do permission. (ie. post_new.)
If boards is specified, checks those boards instead of the current one.
If any is true, will return true if the user has the permission on any of the specified boards
Always returns true if the user is an administrator.

Type|Parameter|Description
---|---|---
`string&#124;array`|`$permission`|A single permission to check or an array of permissions to check
`int&#124;array`|`$boards`|The ID of a board or an array of board IDs if we want to check board-level permissions
`bool`|`$any`|Whether to check for permission on at least one board instead of all boards

### isAllowedTo

```php
function isAllowedTo($permission, $boards = null, $any = false)
```
Fatal error if they cannot.

Uses allowedTo() to check if the user is allowed to do permission.
Checks the passed boards or current board for the permission.
If $any is true, the user only needs permission on at least one of the boards to pass
If they are not, it loads the Errors language file and shows an error using $txt['cannot_' . $permission].
If they are a guest and cannot do it, this calls is_not_guest().

Type|Parameter|Description
---|---|---
`string&#124;array`|`$permission`|A single permission to check or an array of permissions to check
`int&#124;array`|`$boards`|The ID of a single board or an array of board IDs if we're checking board-level permissions (null otherwise)
`bool`|`$any`|Whether to check for permission on at least one board instead of all boards

### boardsAllowedTo

```php
function boardsAllowedTo($permissions, $check_access = true, $simple = true)
```
Return the boards a user has a certain (board) permission on. (array(0) if all.)
 - returns a list of boards on which the user is allowed to do the specified permission.

- returns an array with only a 0 in it if the user has permission to do this on every board.
 - returns an empty array if he or she cannot do this on any board.
If check_access is true will also make sure the group has proper access to that board.

Type|Parameter|Description
---|---|---
`string&#124;array`|`$permissions`|A single permission to check or an array of permissions to check
`bool`|`$check_access`|Whether to check only the boards the user has access to
`bool`|`$simple`|Whether to return a simple array of board IDs or one with permissions as the keys

### spamProtection

```php
function spamProtection($error_type, $only_return_result = true)
```
This function attempts to protect from spammed messages and the like.

The time taken depends on error_type - generally uses the modSetting.

Type|Parameter|Description
---|---|---
`string`|`$error_type`|The error type. Also used as a $txt index (not an actual string).
`bool`|`$only_return_result`|Whether you want the function to die with a fatal_lang_error.

### secureDirectory

```php
function secureDirectory($paths, $attachments = false)
```
A generic function to create a pair of index.php and .htaccess files in a directory



Type|Parameter|Description
---|---|---
`string&#124;array`|`$paths`|The (absolute) directory path
`bool`|`$attachments`|Whether this is an attachment directory

### frameOptionsHeader

```php
function frameOptionsHeader($override = null)
```
This sets the X-Frame-Options header.



Type|Parameter|Description
---|---|---
`string`|`$override`|An option to override (either 'SAMEORIGIN' or 'DENY')

### get_allowed_http_origin

```php
function get_allowed_http_origin($origin)
```
### corsPolicyHeader

```php
function corsPolicyHeader($set_header = true)
```
This sets the Access-Control-Allow-Origin header.



Type|Parameter|Description
---|---|---
`bool`|`$set_header`|(Default: true): When false, we will do the logic, but not send the headers.  The relevant logic is still saved in the $context and can be sent manually.

### FindCorsBaseUrl

```php
function FindCorsBaseUrl($url, $sub_domain = false)
```
Helper function to figure out a urls base domain.

IP addresses are not supported.

Type|Parameter|Description
---|---|---
`string`|`$url`|The url/domain/host we are attempting to vaalidate for the base domain.
`bool`|`$sub_domain`|(Default: false): When true it will lowest level of a domain off before performing any other logic.

### get_domain

```php
function get_domain($hostname)
```
Remove subdomains from hostnames

IP addresses are not supported.

Some example conversions include:

- domain.com -> domain.com
- sub.domain.com -> domain.com
- www.domain.com -> domain.com
- www.sub.sub.domain.com -> domain.com
- domain.co.uk -> domain.co.uk
- sub.domain.co.uk -> domain.co.uk
- www.domain.co.uk -> domain.co.uk
- www.sub.sub.domain.co.uk -> domain.co.uk

Only works well with TLDs that do not use a dot seperator,
although accomodations are made for ccSLDs.

Type|Parameter|Description
---|---|---
`string`|`$hostname`|

