---
layout: default
group: func
navtitle: Register.php
title: ./Sources/Register.php
count: 7
---
* auto-gen TOC:
{:toc}
### Register

```php
function Register($reg_errors = array())
```
Begin the registration process.



Type|Parameter|Description
---|---|---
`array`|`$reg_errors`|Holds information about any errors that occurred

### Register2

```php
function Register2()
```
Actually register the member.



### Activate

```php
function Activate()
```
Activate an users account.

Checks for mail changes, resends password if needed.

### CoppaForm

```php
function CoppaForm()
```
This function will display the contact information for the forum, as well a form to fill in.



### VerificationCode

```php
function VerificationCode()
```
Show the verification code or let it be heard.



### RegisterCheckUsername

```php
function RegisterCheckUsername()
```
See if a username already exists.



### SendActivation

```php
function SendActivation()
```
It doesn't actually send anything, this action just shows a message for a guest.



