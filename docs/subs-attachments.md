---
layout: default
group: func
navtitle: Subs-Attachments.php
title: ./Sources/Subs-Attachments.php
count: 15
---
* auto-gen TOC:
{:toc}
### automanage_attachments_check_directory

```php
function automanage_attachments_check_directory()
```
Check if the current directory is still valid or not.

If not creates the new directory

### automanage_attachments_create_directory

```php
function automanage_attachments_create_directory($updir)
```
Creates a directory



Type|Parameter|Description
---|---|---
`string`|`$updir`|The directory to be created

### is_path_allowed

```php
function is_path_allowed($path)
```
Check if open_basedir restrictions are in effect.

If so check if the path is allowed.

Type|Parameter|Description
---|---|---
`string`|`$path`|The path to check

### automanage_attachments_by_space

```php
function automanage_attachments_by_space()
```
Called when a directory space limit is reached.

Creates a new directory and increments the directory suffix number.

### get_directory_tree_elements

```php
function get_directory_tree_elements($directory)
```
Split a path into a list of all directories and subdirectories



Type|Parameter|Description
---|---|---
`string`|`$directory`|A path

### attachments_init_dir

```php
function attachments_init_dir(&$tree, &$count)
```
Return the first part of a path (i.e. c:\ or / + the first directory), used by automanage_attachments_create_directory



Type|Parameter|Description
---|---|---
`array`|`$tree`|An array
`int`|`$count`|The number of elements in $tree

### processAttachments

```php
function processAttachments()
```
Moves an attachment to the proper directory and set the relevant data into $_SESSION['temp_attachments']



### attachmentChecks

```php
function attachmentChecks($attachID)
```
Performs various checks on an uploaded file.

- Requires that $_SESSION['temp_attachments'][$attachID] be properly populated.

Type|Parameter|Description
---|---|---
`int`|`$attachID`|The ID of the attachment

### createAttachment

```php
function createAttachment(&$attachmentOptions)
```
Create an attachment, with the given array of parameters.

- Adds any additional or missing parameters to $attachmentOptions.
- Renames the temporary file.
- Creates a thumbnail if the file is an image and the option enabled.

Type|Parameter|Description
---|---|---
`array`|`$attachmentOptions`|An array of attachment options

### assignAttachments

```php
function assignAttachments($attachIDs = array(), $msgID = 0)
```
Assigns the given attachments to the given message ID.



Type|Parameter|Description
---|---|---
`null`|`$attachIDs`|array of attachment IDs to assign.
`null`|`$msgID`|integer the message ID.

### parseAttachBBC

```php
function parseAttachBBC($attachID = 0)
```
Gets an attach ID and tries to load all its info.



Type|Parameter|Description
---|---|---
`int`|`$attachID`|the attachment ID to load info from.

### getRawAttachInfo

```php
function getRawAttachInfo($attachIDs)
```
Gets raw info directly from the attachments table.



Type|Parameter|Description
---|---|---
`array`|`$attachIDs`|An array of attachments IDs.

### getAttachMsgInfo

```php
function getAttachMsgInfo($attachID)
```
Gets all needed message data associated with an attach ID



Type|Parameter|Description
---|---|---
`int`|`$attachID`|the attachment ID to load info from.

### loadAttachmentContext

```php
function loadAttachmentContext($id_msg, $attachments)
```
This loads an attachment's contextual data including, most importantly, its size if it is an image.

It requires the view_attachments permission to calculate image size.
It attempts to keep the "aspect ratio" of the posted image in line, even if it has to be resized by
the max_image_width and max_image_height settings.

Type|Parameter|Description
---|---|---
`int`|`$id_msg`|ID of the post to load attachments for
`array`|`$attachments`|An array of already loaded attachments. This function no longer depends on having $topic declared, thus, you need to load the actual topic ID for each attachment.

### prepareAttachsByMsg

```php
function prepareAttachsByMsg($msgIDs)
```
prepare the Attachment api for all messages



Type|Parameter|Description
---|---|---
`int`|``|array $msgIDs the message ID to load info from.

