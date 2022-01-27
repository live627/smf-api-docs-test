---
layout: default
group: hooks
title: ManageAttachments.php
count: 10
---
* auto-gen TOC:
{:toc}
### integrate_manage_attachments

```php
call_integration_hook('integrate_manage_attachments', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`ManageAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageattachments)

Notes
: Since 2.1

### integrate_modify_attachment_settings

```php
call_integration_hook('integrate_modify_attachment_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ManageAttachmentSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageattachmentsettings)

Notes
: Since 2.1

### integrate_save_attachment_settings

```php
call_integration_hook('integrate_save_attachment_settings')
```


Called from
: [`ManageAttachmentSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageattachmentsettings)

Notes
: Since 2.1

### integrate_modify_avatar_settings

```php
call_integration_hook('integrate_modify_avatar_settings', array(&$config_vars))
```

Type|Parameter|Description
---|---|---
`array`|`$&config_vars`|desc

Called from
: [`ManageAvatarSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageavatarsettings)

Notes
: Since 2.1

### integrate_save_avatar_settings

```php
call_integration_hook('integrate_save_avatar_settings')
```


Called from
: [`ManageAvatarSettings()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#manageavatarsettings)

Notes
: Since 2.1

### integrate_attachments_browse

```php
call_integration_hook('integrate_attachments_browse', array(&$listOptions, &$titles, &$list_title))
```

Type|Parameter|Description
---|---|---
`array`|`$&listOptions`|desc
`array`|`$&titles`|desc
`array`|`$&list_title`|desc

Called from
: [`BrowseFiles()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#browsefiles)

Notes
: Since 2.1

### integrate_attachment_remove

```php
call_integration_hook('integrate_attachment_remove', array(&$filesRemoved, $attachments))
```

Type|Parameter|Description
---|---|---
`array`|`$&filesRemoved`|desc
`array`|`$attachments`|desc

Called from
: [`RemoveAttachment()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#removeattachment)

Notes
: Since 2.1

### integrate_remove_attachments

```php
call_integration_hook('integrate_remove_attachments', array($attach))
```

Type|Parameter|Description
---|---|---
`array`|`$attach`|desc

Called from
: [`removeAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#removeattachments)

Notes
: Since 2.1

### integrate_repair_attachments_nomsg

```php
call_integration_hook('integrate_repair_attachments_nomsg', array(&$ignore_ids, $_GET['substep'], $_GET['substep'] + 500))
```

Type|Parameter|Description
---|---|---
`array`|`$&ignore_ids`|desc
`array`|`$substep`|desc
`array`|`???`|desc

Called from
: [`RepairAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#repairattachments)

Notes
: Since 2.1

### integrate_approve_attachments

```php
call_integration_hook('integrate_approve_attachments', array($attachments))
```

Type|Parameter|Description
---|---|---
`array`|`$attachments`|desc

Called from
: [`ApproveAttachments()` in `./Sources/ManageAttachments.php`](../docs/manageattachments.html#approveattachments)

Notes
: Since 2.1

