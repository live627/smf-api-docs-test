---
layout: default
group: func
navtitle: Subs-Auth.php
title: ./Sources/Subs-Auth.php
count: 22
---
* auto-gen TOC:
{:toc}
### setLoginCookie

```php
function setLoginCookie($cookie_length, $id, $password = '')
```
Sets the SMF-style login cookie and session based on the id_member and password passed.

- password should be already encrypted with the cookie salt.
- logs the user out if id_member is zero.
- sets the cookie and session to last the number of seconds specified by cookie_length, or
  ends them if cookie_length is less than 0.
- when logging out, if the globalCookies setting is enabled, attempts to clear the subdomain's
  cookie too.

Type|Parameter|Description
---|---|---
`int`|`$cookie_length`|How many seconds the cookie should last. If negative, forces logout.
`int`|`$id`|The ID of the member to set the cookie for
`string`|`$password`|The hashed password

### setTFACookie

```php
function setTFACookie($cookie_length, $id, $secret)
```
Sets Two Factor Auth cookie



Type|Parameter|Description
---|---|---
`int`|`$cookie_length`|How long the cookie should last, in seconds
`int`|`$id`|The ID of the member
`string`|`$secret`|Should be a salted secret using hash_salt

### url_parts

```php
function url_parts($local, $global)
```
Get the domain and path for the cookie
- normally, local and global should be the localCookies and globalCookies settings, respectively.

- uses boardurl to determine these two things.

Type|Parameter|Description
---|---|---
`bool`|`$local`|Whether we want local cookies
`bool`|`$global`|Whether we want global cookies

### KickGuest

```php
function KickGuest()
```
Throws guests out to the login screen when guest access is off.

- sets $_SESSION['login_url'] to $_SERVER['REQUEST_URL'].
- uses the 'kick_guest' sub template found in Login.template.php.

### InMaintenance

```php
function InMaintenance()
```
Display a message about the forum being in maintenance mode.

- display a login screen with sub template 'maintenance'.
- sends a 503 header, so search engines don't bother indexing while we're in maintenance mode.

### adminLogin

```php
function adminLogin($type = 'admin')
```
Question the verity of the admin by asking for his or her password.

- loads Login.template.php and uses the admin_login sub template.
- sends data to template so the admin is sent on to the page they
  wanted if their password is correct, otherwise they can try again.

Type|Parameter|Description
---|---|---
`string`|`$type`|What login type is this - can be 'admin' or 'moderate'

### adminLogin_outputPostVars

```php
function adminLogin_outputPostVars($k, $v)
```
Used by the adminLogin() function.

if 'value' is an array, the function is called recursively.

Type|Parameter|Description
---|---|---
`string`|`$k`|The keys
`string`|`$v`|The values

### construct_query_string

```php
function construct_query_string($get)
```
Properly urlencodes a string to be used in a query



Type|Parameter|Description
---|---|---
`string`|`$get`|

### findMembers

```php
function findMembers($names, $use_wildcards = false, $buddies_only = false, $max = 500)
```
Finds members by email address, username, or real name.

- searches for members whose username, display name, or e-mail address match the given pattern of array names.
- searches only buddies if buddies_only is set.

Type|Parameter|Description
---|---|---
`array`|`$names`|The names of members to search for
`bool`|`$use_wildcards`|Whether to use wildcards. Accepts wildcards ? and * in the pattern if true
`bool`|`$buddies_only`|Whether to only search for the user's buddies
`int`|`$max`|The maximum number of results

### JSMembers

```php
function JSMembers()
```
Called by index.php?action=findmember.

- is used as a popup for searching members.
- uses sub template find_members of the Help template.
- also used to add members for PM's sent using wap2/imode protocol.

### RequestMembers

```php
function RequestMembers()
```
Outputs each member name on its own line.

- used by javascript to find members matching the request.

### resetPassword

```php
function resetPassword($memID, $username = null)
```
Generates a random password for a user and emails it to them.

- called by Profile.php when changing someone's username.
- checks the validity of the new username.
- generates and sets a new password for the given user.
- mails the new password to the email address of the user.
- if username is not set, only a new password is generated and sent.

Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member
`string`|`$username`|The new username. If set, also checks the validity of the username

### validateUsername

```php
function validateUsername($memID, $username, $return_error = false, $check_reserved_name = true)
```
Checks a username obeys a load of rules



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member
`string`|`$username`|The username to validate
`bool`|`$return_error`|Whether to return errors
`bool`|`$check_reserved_name`|Whether to check this against the list of reserved names

### validatePassword

```php
function validatePassword($password, $username, $restrict_in = array())
```
Checks whether a password meets the current forum rules
- called when registering/choosing a password.

- checks the password obeys the current forum settings for password strength.
- if password checking is enabled, will check that none of the words in restrict_in appear in the password.
- returns an error identifier if the password is invalid, or null.

Type|Parameter|Description
---|---|---
`string`|`$password`|The desired password
`string`|`$username`|The username
`array`|`$restrict_in`|An array of restricted strings that cannot be part of the password (email address, username, etc.)

### rebuildModCache

```php
function rebuildModCache()
```
Quickly find out what moderation authority this user has
- builds the moderator, group and board level querys for the user
- stores the information on the current users moderation powers in $user_info['mod_cache'] and $_SESSION['mc']



### smf_setcookie

```php
function smf_setcookie($name, $value = '', $expire = 0, $path = '', $domain = '', $secure = null, $httponly = true, $samesite = null)
```
A wrapper for setcookie that gives integration hook access to it



Type|Parameter|Description
---|---|---
`string`|`$name`|
`string`|`$value`|= ''
`int`|`$expire`|= 0
`string`|`$path`|= ''
`string`|`$domain`|= ''
`bool`|`$secure`|= false
`bool`|`$httponly`|= true
`string`|`$samesite`|= lax

### hash_password

```php
function hash_password($username, $password, $cost = null)
```
Hashes username with password



Type|Parameter|Description
---|---|---
`string`|`$username`|The username
`string`|`$password`|The unhashed password
`int`|`$cost`|The cost

### hash_salt

```php
function hash_salt($password, $salt)
```
Hashes password with salt and authentication secret. This is solely used for cookies.



Type|Parameter|Description
---|---|---
`string`|`$password`|The password
`string`|`$salt`|The salt

### hash_verify_password

```php
function hash_verify_password($username, $password, $hash)
```
Verifies a raw SMF password against the bcrypt'd string



Type|Parameter|Description
---|---|---
`string`|`$username`|The username
`string`|`$password`|The password
`string`|`$hash`|The hashed string

### hash_length

```php
function hash_length()
```
Returns the length for current hash



### hash_benchmark

```php
function hash_benchmark($hashTime = 0.2)
```
Benchmarks the server to figure out an appropriate cost factor (minimum 9)



Type|Parameter|Description
---|---|---
`float`|`$hashTime`|Time to target, in seconds

### hash_equals

```php
function hash_equals($known_string, $user_string)
```
A compatibility function for when PHP's "hash_equals" function isn't available



Type|Parameter|Description
---|---|---
`string`|`$known_string`|A known hash
`string`|`$user_string`|The hash of the user string

