---
layout: default
group: func
navtitle: Reminder.php
title: ./Sources/Reminder.php
count: 6
---
* auto-gen TOC:
{:toc}
### RemindMe

```php
function RemindMe(): void
```
This is the controlling delegator

Uses Profile language files and Reminder template

### RemindPick

```php
function RemindPick(): void
```
Allows the user to pick how they wish to be reminded



### setPassword

```php
function setPassword(): void
```
Allows the user to set their new password



### setPassword2

```php
function setPassword2(): void
```
Actually sets the new password



Integration hooks
: integrate_reset_pass

### SecretAnswerInput

```php
function SecretAnswerInput(): void
```
Allows the user to enter their secret answer



### SecretAnswer2

```php
function SecretAnswer2(): void
```
Validates the secret answer input by the user



Integration hooks
: integrate_reset_pass

