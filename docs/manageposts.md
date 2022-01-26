---
layout: default
group: func
navtitle: ManagePosts.php
title: ./Sources/ManagePosts.php
count: 5
---
* auto-gen TOC:
{:toc}
### ManagePostSettings

```php
function ManagePostSettings(): void
```
The main entrance point for the 'Posts and topics' screen.

Like all others, it checks permissions, then forwards to the right function
based on the given sub-action.
Defaults to sub-action 'posts'.
Accessed from ?action=admin;area=postsettings.
Requires (and checks for) the admin_forum permission.

### SetCensor

```php
function SetCensor(): void
```
Shows an interface to set and test censored words.

It uses the censor_vulgar, censor_proper, censorWholeWord, and censorIgnoreCase
settings.
Requires the admin_forum permission.
Accessed from ?action=admin;area=postsettings;sa=censor.

### ModifyPostSettings

```php
function ModifyPostSettings(bool $return_config = false): void|array
```
Modify any setting related to posts and posting.

Requires the admin_forum permission.
Accessed from ?action=admin;area=postsettings;sa=posts.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the $config_vars array (used for admin search)

### ModifyTopicSettings

```php
function ModifyTopicSettings(bool $return_config = false): void|array
```
Modify any setting related to topics.

Requires the admin_forum permission.
Accessed from ?action=admin;area=postsettings;sa=topics.

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

### ModifyDraftSettings

```php
function ModifyDraftSettings(bool $return_config = false): void|array
```
Modify any setting related to drafts.

Requires the admin_forum permission.
Accessed from ?action=admin;area=postsettings;sa=drafts

Type|Parameter|Description
---|---|---
`bool`|`$return_config`|Whether or not to return the config_vars array (used for admin search)

