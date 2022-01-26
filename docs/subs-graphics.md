---
layout: default
group: func
navtitle: Subs-Graphics.php
title: ./Sources/Subs-Graphics.php
count: 15
---
* auto-gen TOC:
{:toc}
### downloadAvatar

```php
function downloadAvatar(string $url, int $memID, int $max_width, int $max_height): bool
```
downloads a file from a url and stores it locally for avatar use by id_member.

- supports GIF, JPG, PNG, BMP and WBMP formats.
- detects if GD2 is available.
- uses resizeImageFile() to resize to max_width by max_height, and saves the result to a file.
- updates the database info for the member's avatar.
- returns whether the download and resize was successful.

Type|Parameter|Description
---|---|---
`string`|`$url`|The full path to the temporary file
`int`|`$memID`|The member ID
`int`|`$max_width`|The maximum allowed width for the avatar
`int`|`$max_height`|The maximum allowed height for the avatar

### createThumbnail

```php
function createThumbnail(string $source, int $max_width, int $max_height): bool
```
Create a thumbnail of the given source.



Type|Parameter|Description
---|---|---
`string`|`$source`|The name of the source image
`int`|`$max_width`|The maximum allowed width
`int`|`$max_height`|The maximum allowed height

### reencodeImage

```php
function reencodeImage(string $fileName, int $preferred_format = 0): bool
```
Used to re-econodes an image to a specified image format
- creates a copy of the file at the same location as fileName.

- the file would have the format preferred_format if possible, otherwise the default format is jpeg.
- the function makes sure that all non-essential image contents are disposed.

Type|Parameter|Description
---|---|---
`string`|`$fileName`|The path to the file
`int`|`$preferred_format`|The preferred format - 0 to automatically determine, 1 for gif, 2 for jpg, 3 for png, 6 for bmp and 15 for wbmp

### checkImageContents

```php
function checkImageContents(string $fileName, bool $extensiveCheck = false): bool
```
Searches through the file to see if there's potentially harmful non-binary content.

- if extensiveCheck is true, searches for asp/php short tags as well.

Type|Parameter|Description
---|---|---
`string`|`$fileName`|The path to the file
`bool`|`$extensiveCheck`|Whether to perform extensive checks

### checkGD

```php
function checkGD(): bool
```
Sets a global $gd2 variable needed by some functions to determine
whether the GD2 library is present.



### checkImagick

```php
function checkImagick(): bool
```
Checks whether the Imagick class is present.



### checkMagickWand

```php
function checkMagickWand(): bool
```
Checks whether the MagickWand extension is present.



### imageMemoryCheck

```php
function imageMemoryCheck(array $sizes): bool
```
See if we have enough memory to thumbnail an image



Type|Parameter|Description
---|---|---
`array`|`$sizes`|image size

### resizeImageFile

```php
function resizeImageFile(string $source, string $destination, int $max_width, int $max_height, int $preferred_format = 0): bool
```
Resizes an image from a remote location or a local file.

Puts the resized image at the destination location.
The file would have the format preferred_format if possible,
otherwise the default format is jpeg.

Type|Parameter|Description
---|---|---
`string`|`$source`|The path to the source image
`string`|`$destination`|The path to the destination image
`int`|`$max_width`|The maximum allowed width
`int`|`$max_height`|The maximum allowed height
`int`|`$preferred_format`|- The preferred format (0 to use jpeg, 1 for gif, 2 to force jpeg, 3 for png, 6 for bmp and 15 for wbmp)

### resizeImage

```php
function resizeImage(resource $src_img, string $destName, int $src_width, int $src_height, int $max_width, int $max_height, bool $force_resize = false, int $preferred_format = 0): bool
```
Resizes src_img proportionally to fit within max_width and max_height limits
if it is too large.

If GD2 is present, it'll use it to achieve better quality.
It saves the new image to destination_filename, as preferred_format
if possible, default is jpeg.

Uses Imagemagick (IMagick or MagickWand extension) or GD

Type|Parameter|Description
---|---|---
`resource`|`$src_img`|The source image
`string`|`$destName`|The path to the destination image
`int`|`$src_width`|The width of the source image
`int`|`$src_height`|The height of the source image
`int`|`$max_width`|The maximum allowed width
`int`|`$max_height`|The maximum allowed height
`bool`|`$force_resize`|= false Whether to forcibly resize it
`int`|`$preferred_format`|- 1 for gif, 2 for jpeg, 3 for png, 6 for bmp or 15 for wbmp

### imagecopyresamplebicubic

```php
function imagecopyresamplebicubic(resource $dst_img, resource $src_img, int $dst_x, int $dst_y, int $src_x, int $src_y, int $dst_w, int $dst_h, int $src_w, int $src_h): void
```
Copy image.

Used when imagecopyresample() is not available.

Type|Parameter|Description
---|---|---
`resource`|`$dst_img`|The destination image - a GD image resource
`resource`|`$src_img`|The source image - a GD image resource
`int`|`$dst_x`|The "x" coordinate of the destination image
`int`|`$dst_y`|The "y" coordinate of the destination image
`int`|`$src_x`|The "x" coordinate of the source image
`int`|`$src_y`|The "y" coordinate of the source image
`int`|`$dst_w`|The width of the destination image
`int`|`$dst_h`|The height of the destination image
`int`|`$src_w`|The width of the destination image
`int`|`$src_h`|The height of the destination image

### imagecreatefrombmp

```php
function imagecreatefrombmp(string $filename): resource
```
It is set only if it doesn't already exist (for forwards compatiblity.)
It only supports uncompressed bitmaps.



Type|Parameter|Description
---|---|---
`string`|`$filename`|The name of the file

### gif_outputAsPng

```php
function gif_outputAsPng(\gif_file $gif, string $lpszFileName, int $background_color = -1): bool
```
Writes a gif file to disk as a png file.



Type|Parameter|Description
---|---|---
`\gif_file`|`$gif`|A gif image resource
`string`|`$lpszFileName`|The name of the file
`int`|`$background_color`|The background color

### showCodeImage

```php
function showCodeImage(string $code): void|false
```
Show an image containing the visual verification code for registration.

Requires the GD extension.
Uses a random font for each letter from default_theme_dir/fonts.
Outputs a gif or a png (depending on whether gif ix supported).

Type|Parameter|Description
---|---|---
`string`|`$code`|The code to display

### showLetterImage

```php
function showLetterImage(string $letter): void|false
```
Show a letter for the visual verification code.

Alternative function for showCodeImage() in case GD is missing.
Includes an image from a random sub directory of default_theme_dir/fonts.

Type|Parameter|Description
---|---|---
`string`|`$letter`|A letter to show as an image

