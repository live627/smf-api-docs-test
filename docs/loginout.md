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
function Login(): void
```
Ask them for their login information. (shows a page for the user to type
 in their username and password.)
 It caches the referring URL in $_SESSION['login_url'].

It is accessed from ?action=login.

Uses Login template and language file with the login sub-template.

### Login2

```php
function Login2(): void
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

Integration hooks
: integrate_validate_login
: integrate_other_passwords

### LoginTFA

```php
function LoginTFA(): void
```
Allows the user to enter their Two-Factor Authentication code



### checkActivation

```php
function checkActivation(): void
```
Check activation status of the current user.



### DoLogin

```php
function DoLogin(): void
```
Perform the logging in. (set cookie, call hooks, etc)



Integration hooks
: integrate_login

### Logout

```php
function Logout(bool $internal = false, bool $redirect = true): void
```
Logs the current user out of their account.

It requires that the session hash is sent as well, to prevent automatic logouts by images or javascript.
It redirects back to $_SESSION['logout_url'], if it exists.
It is accessed via ?action=logout;session_var=...

Type|Parameter|Description
---|---|---
`bool`|`$internal`|If true, it doesn't check the session
`bool`|`$redirect`|Whether or not to redirect the user after they log out

Integration hooks
: integrate_logout

### md5_hmac

```php
function md5_hmac(string $data, string $key): string
```
MD5 Encryption used for older passwords. (SMF 1.0.x/YaBB SE 1.5.x hashing)



Type|Parameter|Description
---|---|---
`string`|`$data`|The data
`string`|`$key`|The key

### phpBB3_password_check

```php
function phpBB3_password_check(string $passwd, string $passwd_hash): string
```
Custom encryption for phpBB3 based passwords.



Type|Parameter|Description
---|---|---
`string`|`$passwd`|The raw \(unhashed\) password
`string`|`$passwd_hash`|The hashed password

### validatePasswordFlood

```php
function validatePasswordFlood(int $id_member, string $member_name, bool|string $password_flood_value = false, bool $was_correct = false, bool $tfa = false): void
```
This protects against brute force attacks on a member's password.

Importantly, even if the password was right we DON'T TELL THEM!

Type|Parameter|Description
---|---|---
`int`|`$id_member`|The ID of the member
`string`|`$member_name`|The name of the member\.
`bool`&#124;`string`|`$password_flood_value`|False if we don't have a flood value, otherwise a string with a timestamp and number of tries separated by a |
`bool`|`$was_correct`|Whether or not the password was correct
`bool`|`$tfa`|Whether we're validating for two\-factor authentication

