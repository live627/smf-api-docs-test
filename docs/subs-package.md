---
layout: default
group: func
navtitle: Subs-Package.php
title: ./Sources/Subs-Package.php
count: 30
---
* auto-gen TOC:
{:toc}
### read_tgz_file

```php
function read_tgz_file(string $gzfilename, string $destination, bool $single_file = false, bool $overwrite = false, ?array $files_to_extract = null): array|false
```
Reads an archive from either a remote location or from the local filesystem.



Type|Parameter|Description
---|---|---
`string`|`$gzfilename`|The path to the tar.gz file
`string`|`$destination`|The path to the desitnation directory
`bool`|`$single_file`|If true returns the contents of the file specified by destination if it exists
`bool`|`$overwrite`|Whether to overwrite existing files
`null`&#124;`array`|`$files_to_extract`|Specific files to extract

### read_tgz_data

```php
function read_tgz_data(string $data, ?string $destination, bool $single_file = false, bool $overwrite = false, ?array $files_to_extract = null): array|false
```
Extracts a file or files from the .tar.gz contained in data.

detects if the file is really a .zip file, and if so returns the result of read_zip_data

if destination is null
- returns a list of files in the archive.

if single_file is true
- returns the contents of the file specified by destination, if it exists, or false.
- destination can start with * and / to signify that the file may come from any directory.
- destination should not begin with a / if single_file is true.

overwrites existing files with newer modification times if and only if overwrite is true.
creates the destination directory if it doesn't exist, and is is specified.
requires zlib support be built into PHP.
returns an array of the files extracted.
if files_to_extract is not equal to null only extracts file within this array.

Type|Parameter|Description
---|---|---
`string`|`$data`|The gzipped tarball
`null`&#124;`string`|`$destination`|The destination
`bool`|`$single_file`|Whether to only extract a single file
`bool`|`$overwrite`|Whether to overwrite existing data
`null`&#124;`array`|`$files_to_extract`|If set, only extracts the specified files

### read_zip_data

```php
function read_zip_data(string $data, string $destination, bool $single_file = false, bool $overwrite = false, array $files_to_extract = null): mixed
```
Extract zip data.

If single_file is true, destination can start with * and / to signify that the file may come from any directory.
Destination should not begin with a / if single_file is true.

Type|Parameter|Description
---|---|---
`string`|`$data`|ZIP data
`string`|`$destination`|Null to display a listing of files in the archive, the destination for the files in the archive or the name of a single file to display (if $single_file is true)
`bool`|`$single_file`|If true, returns the contents of the file specified by destination or false if the file can't be found (default value is false).
`bool`|`$overwrite`|If true, will overwrite files with newer modication times. Default is false.
`array`|`$files_to_extract`|

### url_exists

```php
function url_exists(string $url): bool
```
Checks the existence of a remote file since file_exists() does not do remote.

will return false if the file is "moved permanently" or similar.

Type|Parameter|Description
---|---|---
`string`|`$url`|The URL to parse

### loadInstalledPackages

```php
function loadInstalledPackages(): array
```
Loads and returns an array of installed packages.

default sort order is package_installed time

### getPackageInfo

```php
function getPackageInfo(string $gzfilename): array|string
```
Loads a package's information and returns a representative array.

- expects the file to be a package in Packages/.
- returns a error string if the package-info is invalid.
- otherwise returns a basic array of id, version, filename, and similar information.
- an xmlArray is available in 'xml'.

Type|Parameter|Description
---|---|---
`string`|`$gzfilename`|The path to the file

### create_chmod_control

```php
function create_chmod_control(array $chmodFiles = array(), array $chmodOptions = array(), bool $restore_write_status = false): array
```
Create a chmod control for chmoding files.



Type|Parameter|Description
---|---|---
`array`|`$chmodFiles`|Which files to chmod
`array`|`$chmodOptions`|Options for chmod
`bool`|`$restore_write_status`|Whether to restore write status

### packageRequireFTP

```php
function packageRequireFTP(string $destination_url, ?array $files = null, bool $return = false): array
```
Use FTP functions to work with a package download/install



Type|Parameter|Description
---|---|---
`string`|`$destination_url`|The destination URL
`null`&#124;`array`|`$files`|The files to CHMOD
`bool`|`$return`|Whether to return an array of file info if there's an error

### parsePackageInfo

```php
function parsePackageInfo(\xmlArray &$packageXML, bool $testing_only = true, string $method = 'install', string $previous_version = ''): array
```
Parses the actions in package-info.xml file from packages.

- package should be an xmlArray with package-info as its base.
- testing_only should be true if the package should not actually be applied.
- method can be upgrade, install, or uninstall.  Its default is install.
- previous_version should be set to the previous installed version of this package, if any.
- does not handle failure terribly well; testing first is always better.

Type|Parameter|Description
---|---|---
`\xmlArray`|` &$packageXML`|The info from the package-info file
`bool`|`$testing_only`|Whether we're only testing
`string`|`$method`|The method ('install', 'upgrade', or 'uninstall')
`string`|`$previous_version`|The previous version of the mod, if method is 'upgrade'

### matchHighestPackageVersion

```php
function matchHighestPackageVersion(string $versions, bool $reset, string $the_version): string|bool
```
Checks if version matches any of the versions in `$versions`.

- supports comma separated version numbers, with or without whitespace.
- supports lower and upper bounds. (1.0-1.2)
- returns true if the version matched.

Type|Parameter|Description
---|---|---
`string`|`$versions`|The versions that this package will install on
`bool`|`$reset`|Whether to reset $near_version
`string`|`$the_version`|The forum version

### matchPackageVersion

```php
function matchPackageVersion(string $version, string $versions): bool
```
Checks if the forum version matches any of the available versions from the package install xml.

- supports comma separated version numbers, with or without whitespace.
- supports lower and upper bounds. (1.0-1.2)
- returns true if the version matched.

Type|Parameter|Description
---|---|---
`string`|`$version`|The forum version
`string`|`$versions`|The versions that this package will install on

### compareVersions

```php
function compareVersions(string $version1, string $version2): int
```
Compares two versions and determines if one is newer, older or the same, returns
- (-1) if version1 is lower than version2
- (0) if version1 is equal to version2
- (1) if version1 is higher than version2



Type|Parameter|Description
---|---|---
`string`|`$version1`|The first version
`string`|`$version2`|The second version

### parse_path

```php
function parse_path(string $path): string
```
Parses special identifiers out of the specified path.



Type|Parameter|Description
---|---|---
`string`|`$path`|The path

### deltree

```php
function deltree(string $dir, bool $delete_dir = true): void
```
Deletes a directory, and all the files and direcories inside it.

requires access to delete these files.

Type|Parameter|Description
---|---|---
`string`|`$dir`|A directory
`bool`|`$delete_dir`|If false, only deletes everything inside the directory but not the directory itself

### mktree

```php
function mktree(string $strPath, int $mode): bool
```
Creates the specified tree structure with the mode specified.

creates every directory in path until it finds one that already exists.

Type|Parameter|Description
---|---|---
`string`|`$strPath`|The path
`int`|`$mode`|The permission mode for CHMOD (0666, etc.)

### copytree

```php
function copytree(string $source, string $destination): void
```
Copies one directory structure over to another.

requires the destination to be writable.

Type|Parameter|Description
---|---|---
`string`|`$source`|The directory to copy
`string`|`$destination`|The directory to copy $source to

### listtree

```php
function listtree(string $path, string $sub_path = ''): array
```
Create a tree listing for a given directory path



Type|Parameter|Description
---|---|---
`string`|`$path`|The path
`string`|`$sub_path`|The sub-path

### parseModification

```php
function parseModification(string $file, bool $testing = true, bool $undo = false, array $theme_paths = array()): array
```
Parses a xml-style modification file (file).



Type|Parameter|Description
---|---|---
`string`|`$file`|The modification file to parse
`bool`|`$testing`|Whether we're just doing a test
`bool`|`$undo`|If true, specifies that the modifications should be undone. Used when uninstalling. Doesn't work with regex.
`array`|`$theme_paths`|An array of information about custom themes to apply the changes to

### parseBoardMod

```php
function parseBoardMod(string $file, bool $testing = true, bool $undo = false, array $theme_paths = array()): array
```
Parses a boardmod-style (.mod) modification file



Type|Parameter|Description
---|---|---
`string`|`$file`|The modification file to parse
`bool`|`$testing`|Whether we're just doing a test
`bool`|`$undo`|If true, specifies that the modifications should be undone. Used when uninstalling.
`array`|`$theme_paths`|An array of information about custom themes to apply the changes to

### package_get_contents

```php
function package_get_contents(string $filename): string
```
Get the physical contents of a packages file



Type|Parameter|Description
---|---|---
`string`|`$filename`|The package file

### package_put_contents

```php
function package_put_contents(string $filename, string $data, bool $testing = false): int
```
Writes data to a file, almost exactly like the file_put_contents() function.

uses FTP to create/chmod the file when necessary and available.
uses text mode for text mode file extensions.
returns the number of bytes written.

Type|Parameter|Description
---|---|---
`string`|`$filename`|The name of the file
`string`|`$data`|The data to write to the file
`bool`|`$testing`|Whether we're just testing things

### package_flush_cache

```php
function package_flush_cache(bool $trash = false): void
```
Flushes the cache from memory to the filesystem



Type|Parameter|Description
---|---|---
`bool`|`$trash`|

### package_chmod

```php
function package_chmod(string $filename, string $perm_state = 'writable', bool $track_change = false): bool
```
Try to make a file writable.



Type|Parameter|Description
---|---|---
`string`|`$filename`|The name of the file
`string`|`$perm_state`|The permission state - can be either 'writable' or 'execute'
`bool`|`$track_change`|Whether to track this change

### package_crypt

```php
function package_crypt(string $pass): string
```
Used to crypt the supplied ftp password in this session



Type|Parameter|Description
---|---|---
`string`|`$pass`|The password

### package_unique_filename

```php
function package_unique_filename(string $dir, string $filename, string $ext): string
```




Type|Parameter|Description
---|---|---
`string`|`$dir`|
`string`|`$filename`|The filename without an extension
`string`|`$ext`|

### package_create_backup

```php
function package_create_backup(string $id = 'backup'): bool
```
Creates a backup of forum files prior to modifying them



Type|Parameter|Description
---|---|---
`string`|`$id`|The name of the backup

### smf_crc32

```php
function smf_crc32(string $number): string
```
crc32 doesn't work as expected on 64-bit functions - make our own.

https://php.net/crc32#79567

Type|Parameter|Description
---|---|---
`string`|`$number`|

### package_validate_installtest

```php
function package_validate_installtest(array $package): array
```
Validate a package during install



Type|Parameter|Description
---|---|---
`array`|`$package`|Package data

### package_validate

```php
function package_validate(array $packages): array
```
Validate multiple packages.



Type|Parameter|Description
---|---|---
`array`|`$packages`|Package data

### package_validate_send

```php
function package_validate_send(array $sendData): array
```
Sending data off to validate packages.



Type|Parameter|Description
---|---|---
`array`|`$sendData`|Json encoded data to be sent to the validation servers.

