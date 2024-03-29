---
layout: default
group: func
navtitle: ManageRegistration.php
title: ./Sources/ManageRegistration.php
count: 6
---
* auto-gen TOC:
{:toc}
### RegCenter

```php
function RegCenter(): void
```
Entrance point for the registration center, it checks permissions and forwards
to the right function based on the subaction.

Accessed by ?action=admin;area=regcenter.
Requires either the moderate_forum or the admin_forum permission.

Uses Login language file
Uses Register template.

Integration hooks
: integrate_manage_registrations

### AdminRegister

```php
function AdminRegister(): void
```
This function allows the admin to register a new member by hand.

It also allows assigning a primary group to the member being registered.
Accessed by ?action=admin;area=regcenter;sa=register
Requires the moderate_forum permission.

### EditAgreement

```php
function EditAgreement(): void
```
Allows the administrator to edit the registration agreement, and choose whether
it should be shown or not. It writes and saves the agreement to the agreement.txt
file.

Accessed by ?action=admin;area=regcenter;sa=agreement.
Requires the admin_forum permission.

### SetReserved

```php
function SetReserved(): void
```
Set the names under which users are not allowed to register.

Accessed by ?action=admin;area=regcenter;sa=reservednames.
Requires the admin_forum permission.

### ModifyRegistrationSettings

```php
function ModifyRegistrationSettings(bool $return_config = false): void|array
```
This function handles registration settings, and provides a few pretty stats too while it's at it.

General registration settings and Coppa compliance settings.
Accessed by ?action=admin;area=regcenter;sa=settings.
Requires the admin_forum permission.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

Integration hooks
: integrate_modify_registration_settings
: integrate_save_registration_settings

### EditPrivacyPolicy

```php
// Sure, you can sell my personal info for profit (...or not)
function EditPrivacyPolicy()
```
