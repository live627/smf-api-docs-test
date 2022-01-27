---
layout: default
group: func
navtitle: Profile.php
title: ./Sources/Profile.php
count: 4
---
* auto-gen TOC:
{:toc}
### ModifyProfile

```php
function ModifyProfile(array $post_errors = array()): void
```
The main designating function for modifying profiles. Loads up info, determins what to do, etc.



Type|Parameter|Description
---|---|---
`array`|`$post_errors`|Any errors that occurred

Integration hooks
: integrate_pre_profile_areas
: integrate_verify_password
: integrate_profile_save
: integrate_reset_pass

### profile_popup

```php
function profile_popup(int $memID): void
```
Set up the requirements for the profile popup - the area that is shown as the popup menu for the current user.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

Integration hooks
: integrate_profile_popup

### alerts_popup

```php
function alerts_popup(int $memID): void
```
Set up the requirements for the alerts popup - the area that shows all the alerts just quickly for the current user.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member

### loadCustomFields

```php
function loadCustomFields(int $memID, string $area = 'summary'): void
```
Load any custom fields for this area... no area means load all, 'summary' loads all public ones.



Type|Parameter|Description
---|---|---
`int`|`$memID`|The ID of the member
`string`|`$area`|Which area to load fields for

Integration hooks
: integrate_load_custom_profile_fields

