---
layout: default
title: Profile.php
count: 4
---

# ./Sources/Profile.php

### ModifyProfile

```php
function ModifyProfile($post_errors = array())
```
The main designating function for modifying profiles. Loads up info, determins what to do, etc.



Type|Parameter|Name
---|---|---
array|$post_errors|Any errors that occurred

### profile_popup

```php
function profile_popup($memID)
```
Set up the requirements for the profile popup - the area that is shown as the popup menu for the current user.



Type|Parameter|Name
---|---|---
int|$memID|The ID of the member

### alerts_popup

```php
function alerts_popup($memID)
```
Set up the requirements for the alerts popup - the area that shows all the alerts just quickly for the current user.



Type|Parameter|Name
---|---|---
int|$memID|The ID of the member

### loadCustomFields

```php
function loadCustomFields($memID, $area = 'summary')
```
Load any custom fields for this area... no area means load all, 'summary' loads all public ones.



Type|Parameter|Name
---|---|---
int|$memID|The ID of the member
string|$area|Which area to load fields for

