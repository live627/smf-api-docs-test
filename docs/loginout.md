---
layout: default
group: func
navtitle: LogInOut.php
title: ./Sources/LogInOut.php
count: 9
---
* auto-gen TOC:
{:toc}
### Login

```php
function Login()
```
Ask them for their login information. (shows a page for the user to type
 in their username and password.)
 It caches the referring URL in $_SESSION['login_url'].

It is accessed from ?action=login.

Uses Login template and language file with the login sub-template.

### Login2

```php
function Login2()
```
Actually logs you in.

What it does:
- checks credentials and checks that login was successful.
- it employs protection against a specific IP or user trying to brute force
 a login to an account.
- upgrades password encryption on login, if necessary.
- after successful login, redirects you to $_SESSION['login_url'].
- accessed from ?action=login2, by forms.
On error, uses the same templates Login() uses.

### LoginTFA

```php
function LoginTFA()
```
Allows the user to enter their Two-Factor Authentication code



### checkActivation

```php
function checkActivation()
```
Check activation status of the current user.



### DoLogin

```php
function DoLogin()
```
Perform the logging in. (set cookie, call hooks, etc)



### Logout

```php
function Logout($internal = false, $redirect = true)
```
Logs the current user out of their account.

It requires that the session hash is sent as well, to prevent automatic logouts by images or javascript.
It redirects back to $_SESSION['logout_url'], if it exists.
It is accessed via ?action=logout;session_var=...

Type|Parameter|Description
---|---|---
`bool`|`$internal`|If true, it doesn't check the session
`bool`|`$redirect`|Whether or not to redirect the user after they log out

### md5_hmac

```php
function md5_hmac($data, $key)
```
MD5 Encryption used for older passwords. (SMF 1.0.x/YaBB SE 1.5.x hashing)



Type|Parameter|Description
---|---|---
`string`|`$data`|The data
`string`|`$key`|The key

### phpBB3_password_check

```php
function phpBB3_password_check($passwd, $passwd_hash)
```
Custom encryption for phpBB3 based passwords.



Type|Parameter|Description
---|---|---
`string`|`$passwd`|The raw (unhashed) password
`string`|`$passwd_hash`|The hashed password

### validatePasswordFlood

```php
function validatePasswordFlood($id_member, $member_name, $password_flood_value = false, $was_correct = false, $tfa = false)
```
This protects against brute force attacks on a member's password.

Importantly, even if the password was right we DON'T TELL THEM!

Type|Parameter|Description
---|---|---
`int`|`$id_member`|The ID of the member
`string`|`$member_name`|The name of the member.
`bool&#124;string`|`$password_flood_value`|False if we don't have a flood value, otherwise a string with a timestamp and number of tries separated by a |
`bool`|`$was_correct`|Whether or not the password was correct
`bool`|`$tfa`|Whether we're validating for two-factor authentication

