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
function Register(array $reg_errors = array()): void
```
Begin the registration process.



Type|Parameter|Description
---|---|---
`array`|`$reg_errors`|Holds information about any errors that occurred

### Register2

```php
function Register2(): void
```
Actually register the member.



### Activate

```php
function Activate(): void
```
Activate an users account.

Checks for mail changes, resends password if needed.

### CoppaForm

```php
function CoppaForm(): void
```
This function will display the contact information for the forum, as well a form to fill in.



### VerificationCode

```php
function VerificationCode(): void
```
Show the verification code or let it be heard.



### RegisterCheckUsername

```php
function RegisterCheckUsername(): void
```
See if a username already exists.



### SendActivation

```php
function SendActivation(): void
```
It doesn't actually send anything, this action just shows a message for a guest.



