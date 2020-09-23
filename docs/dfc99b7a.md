---
layout: default
title: Subs-Graphics.php
count: 15
---

# ./Sources/Subs-Graphics.php

### downloadAvatar

```php
function downloadAvatar($url, $memID, $max_width, $max_height)
```
downloads a file from a url and stores it locally for avatar use by id_member.

- supports GIF, JPG, PNG, BMP and WBMP formats.
- detects if GD2 is available.
- uses resizeImageFile() to resize to max_width by max_height, and saves the result to a file.
- updates the database info for the member's avatar.
- returns whether the download and resize was successful.

Type|Parameter|Name
---|---|---
string|$url|The full path to the temporary file
int|$memID|The member ID
int|$max_width|The maximum allowed width for the avatar
int|$max_height|The maximum allowed height for the avatar

### createThumbnail

```php
function createThumbnail($source, $max_width, $max_height)
```
Create a thumbnail of the given source.



Type|Parameter|Name
---|---|---
string|$source|The name of the source image
int|$max_width|The maximum allowed width
int|$max_height|The maximum allowed height

### reencodeImage

```php
function reencodeImage($fileName, $preferred_format = 0)
```
Used to re-econodes an image to a specified image format
- creates a copy of the file at the same location as fileName.

- the file would have the format preferred_format if possible, otherwise the default format is jpeg.
- the function makes sure that all non-essential image contents are disposed.

Type|Parameter|Name
---|---|---
string|$fileName|The path to the file
int|$preferred_format|The preferred format - 0 to automatically determine, 1 for gif, 2 for jpg, 3 for png, 6 for bmp and 15 for wbmp

### checkImageContents

```php
function checkImageContents($fileName, $extensiveCheck = false)
```
Searches through the file to see if there's potentially harmful non-binary content.

- if extensiveCheck is true, searches for asp/php short tags as well.

Type|Parameter|Name
---|---|---
string|$fileName|The path to the file
bool|$extensiveCheck|Whether to perform extensive checks

### checkGD

```php
function checkGD()
```
Sets a global $gd2 variable needed by some functions to determine
whether the GD2 library is present.




### checkImagick

```php
function checkImagick()
```
Checks whether the Imagick class is present.




### checkMagickWand

```php
function checkMagickWand()
```
Checks whether the MagickWand extension is present.




### imageMemoryCheck

```php
function imageMemoryCheck($sizes)
```
See if we have enough memory to thumbnail an image



Type|Parameter|Name
---|---|---
array|$sizes|image size

### resizeImageFile

```php
function resizeImageFile($source, $destination, $max_width, $max_height, $preferred_format = 0)
```
Resizes an image from a remote location or a local file.

Puts the resized image at the destination location.
The file would have the format preferred_format if possible,
otherwise the default format is jpeg.

Type|Parameter|Name
---|---|---
string|$source|The path to the source image
string|$destination|The path to the destination image
int|$max_width|The maximum allowed width
int|$max_height|The maximum allowed height
int|$preferred_format|- The preferred format (0 to use jpeg, 1 for gif, 2 to force jpeg, 3 for png, 6 for bmp and 15 for wbmp)

### resizeImage

```php
function resizeImage($src_img, $destName, $src_width, $src_height, $max_width, $max_height, $force_resize = false, $preferred_format = 0)
```
Resizes src_img proportionally to fit within max_width and max_height limits
if it is too large.

If GD2 is present, it'll use it to achieve better quality.
It saves the new image to destination_filename, as preferred_format
if possible, default is jpeg.

Uses Imagemagick (IMagick or MagickWand extension) or GD

Type|Parameter|Name
---|---|---
resource|$src_img|The source image
string|$destName|The path to the destination image
int|$src_width|The width of the source image
int|$src_height|The height of the source image
int|$max_width|The maximum allowed width
int|$max_height|The maximum allowed height
bool|$force_resize|= false Whether to forcibly resize it
int|$preferred_format|- 1 for gif, 2 for jpeg, 3 for png, 6 for bmp or 15 for wbmp

### imagecopyresamplebicubic

```php
function imagecopyresamplebicubic($dst_img, $src_img, $dst_x, $dst_y, $src_x, $src_y, $dst_w, $dst_h, $src_w, $src_h)
```
Copy image.

Used when imagecopyresample() is not available.

Type|Parameter|Name
---|---|---
resource|$dst_img|The destination image - a GD image resource
resource|$src_img|The source image - a GD image resource
int|$dst_x|The "x" coordinate of the destination image
int|$dst_y|The "y" coordinate of the destination image
int|$src_x|The "x" coordinate of the source image
int|$src_y|The "y" coordinate of the source image
int|$dst_w|The width of the destination image
int|$dst_h|The height of the destination image
int|$src_w|The width of the destination image
int|$src_h|The height of the destination image

### imagecreatefrombmp

```php
function imagecreatefrombmp($filename)
```
It is set only if it doesn't already exist (for forwards compatiblity.)
It only supports uncompressed bitmaps.



Type|Parameter|Name
---|---|---
string|$filename|The name of the file

### gif_outputAsPng

```php
function gif_outputAsPng($gif, $lpszFileName, $background_color = -1)
```
Writes a gif file to disk as a png file.



Type|Parameter|Name
---|---|---
\gif_file|$gif|A gif image resource
string|$lpszFileName|The name of the file
int|$background_color|The background color

### showCodeImage

```php
function showCodeImage($code)
```
Show an image containing the visual verification code for registration.

Requires the GD extension.
Uses a random font for each letter from default_theme_dir/fonts.
Outputs a gif or a png (depending on whether gif ix supported).

Type|Parameter|Name
---|---|---
string|$code|The code to display

### showLetterImage

```php
function showLetterImage($letter)
```
Show a letter for the visual verification code.

Alternative function for showCodeImage() in case GD is missing.
Includes an image from a random sub directory of default_theme_dir/fonts.

Type|Parameter|Name
---|---|---
string|$letter|A letter to show as an image

