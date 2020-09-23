---
layout: default
title: ./Sources/Load.php
count: 31
---

### reloadSettings

```php
function reloadSettings()
```
Load the $modSettings array.



### loadUserSettings

```php
function loadUserSettings()
```
Load all the important user information.

What it does:
- sets up the $user_info array
- assigns $user_info['query_wanna_see_board'] for what boards the user can see.
- first checks for cookie or integration validation.
- uses the current session if no integration function or cookie is found.
- checks password length, if member is activated and the login span isn't over.
	- if validation fails for the user, $id_member is set to 0.
	- updates the last visit time when needed.

### loadMinUserInfo

```php
function loadMinUserInfo($user_ids = array())
```
Load minimal user info from members table.

Intended for use by background tasks that need to populate $user_info.

Type|Parameter|Description
---|---|---
`int&#124;array`|`$user_ids`|The users IDs to get the data for.

### loadBoard

```php
function loadBoard()
```
Check for moderators and see if they have access to the board.

What it does:
- sets up the $board_info array for current board information.
- if cache is enabled, the $board_info array is stored in cache.
- redirects to appropriate post if only message id is requested.
- is only used when inside a topic or board.
- determines the local moderators for the board.
- adds group id 3 if the user is a local moderator for the board they are in.
- prevents access if user is not in proper group nor a local moderator of the board.

### loadPermissions

```php
function loadPermissions()
```
Load this user's permissions.



### loadMemberData

```php
function loadMemberData($users, $is_name = false, $set = 'normal')
```
Loads an array of users' data by ID or member_name.



Type|Parameter|Description
---|---|---
`array&#124;string`|`$users`|An array of users by id or name or a single username/id
`bool`|`$is_name`|Whether $users contains names
`string`|`$set`|What kind of data to load (normal, profile, minimal)

### loadMemberContext

```php
function loadMemberContext($user, $display_custom_fields = false)
```
Loads the user's basic values... meant for template/theme usage.



Type|Parameter|Description
---|---|---
`int`|`$user`|The ID of a user previously loaded by {@link loadMemberData()}
`bool`|`$display_custom_fields`|Whether or not to display custom profile fields

### loadMemberCustomFields

```php
function loadMemberCustomFields($users, $params)
```
Loads the user's custom profile fields



Type|Parameter|Description
---|---|---
`int&#124;array`|`$users`|A single user ID or an array of user IDs
`string&#124;array`|`$params`|Either a string or an array of strings with profile field names

### detectBrowser

```php
function detectBrowser()
```
Loads information about what browser the user is viewing with and places it in $context
 - uses the class from {@link Class-BrowserDetect.php}



### isBrowser

```php
function isBrowser($browser)
```
Are we using this browser?

Wrapper function for detectBrowser

Type|Parameter|Description
---|---|---
`string`|`$browser`|The browser we are checking for.

### loadTheme

```php
function loadTheme($id_theme = 0, $initialize = true)
```
Load a theme, by ID.



Type|Parameter|Description
---|---|---
`int`|`$id_theme`|The ID of the theme to load
`bool`|`$initialize`|Whether or not to initialize a bunch of theme-related variables/settings

### loadTemplate

```php
function loadTemplate($template_name, $style_sheets = array(), $fatal = true)
```
Load a template - if the theme doesn't include it, use the default.

What this function does:
- loads a template file with the name template_name from the current, default, or base theme.
- detects a wrong default theme directory and tries to work around it.

Type|Parameter|Description
---|---|---
`string`|`$template_name`|The name of the template to load
`array&#124;string`|`$style_sheets`|The name of a single stylesheet or an array of names of stylesheets to load
`bool`|`$fatal`|If true, dies with an error message if the template cannot be found

### loadSubTemplate

```php
function loadSubTemplate($sub_template_name, $fatal = false)
```
Load a sub-template.

What it does:
	- loads the sub template specified by sub_template_name, which must be in an already-loaded template.
 - if ?debug is in the query string, shows administrators a marker after every sub template
for debugging purposes.

Type|Parameter|Description
---|---|---
`string`|`$sub_template_name`|The name of the sub-template to load
`bool`|`$fatal`|Whether to die with an error if the sub-template can't be loaded

### loadCSSFile

```php
function loadCSSFile($fileName, $params = array(), $id = '')
```
Add a CSS file for output later



Type|Parameter|Description
---|---|---
`string`|`$fileName`|The name of the file to load
`array`|`$params`|An array of parameters
Keys are the following:
	- ['external'] (true/false): define if the file is a externally located file. Needs to be set to true if you are loading an external file
	- ['default_theme'] (true/false): force use of default theme url
	- ['force_current'] (true/false): if this is false, we will attempt to load the file from the default theme if not found in the current theme
 - ['validate'] (true/false): if true script will validate the local file exists
 - ['rtl'] (string): additional file to load in RTL mode
 - ['seed'] (true/false/string): if true or null, use cache stale, false do not, or used a supplied string
 - ['minimize'] boolean to add your file to the main minimized file. Useful when you have a file thats loaded everywhere and for everyone.
 - ['order_pos'] int define the load order, when not define it's loaded in the middle, before index.css = -500, after index.css = 500, middle = 3000, end (i.e. after responsive.css) = 10000
 - ['attributes'] array extra attributes to add to the element
`string`|`$id`|An ID to stick on the end of the filename for caching purposes

### addInlineCss

```php
function addInlineCss($css)
```
Add a block of inline css code to be executed later

- only use this if you have to, generally external css files are better, but for very small changes
  or for scripts that require help from PHP/whatever, this can be useful.
- all code added with this function is added to the same <style> tag so do make sure your css is valid!

Type|Parameter|Description
---|---|---
`string`|`$css`|Some css code

### loadJavaScriptFile

```php
function loadJavaScriptFile($fileName, $params = array(), $id = '')
```
Add a Javascript file for output later



Type|Parameter|Description
---|---|---
`string`|`$fileName`|The name of the file to load
`array`|`$params`|An array of parameter info
Keys are the following:
	- ['external'] (true/false): define if the file is a externally located file. Needs to be set to true if you are loading an external file
	- ['default_theme'] (true/false): force use of default theme url
	- ['defer'] (true/false): define if the file should load in <head> or before the closing <html> tag
	- ['force_current'] (true/false): if this is false, we will attempt to load the file from the
default theme if not found in the current theme
- ['async'] (true/false): if the script should be loaded asynchronously (HTML5)
 - ['validate'] (true/false): if true script will validate the local file exists
 - ['seed'] (true/false/string): if true or null, use cache stale, false do not, or used a supplied string
 - ['minimize'] boolean to add your file to the main minimized file. Useful when you have a file thats loaded everywhere and for everyone.
 - ['attributes'] array extra attributes to add to the element
`string`|`$id`|An ID to stick on the end of the filename

### addJavaScriptVar

```php
function addJavaScriptVar($key, $value, $escape = false)
```
Add a Javascript variable for output later (for feeding text strings and similar to JS)
Cleaner and easier (for modders) than to use the function below.



Type|Parameter|Description
---|---|---
`string`|`$key`|The key for this variable
`string`|`$value`|The value
`bool`|`$escape`|Whether or not to escape the value

### addInlineJavaScript

```php
function addInlineJavaScript($javascript, $defer = false)
```
Add a block of inline Javascript code to be executed later

- only use this if you have to, generally external JS files are better, but for very small scripts
  or for scripts that require help from PHP/whatever, this can be useful.
- all code added with this function is added to the same <script> tag so do make sure your JS is clean!

Type|Parameter|Description
---|---|---
`string`|`$javascript`|Some JS code
`bool`|`$defer`|Whether the script should load in <head> or before the closing <html> tag

### loadLanguage

```php
function loadLanguage($template_name, $lang = '', $fatal = true, $force_reload = false)
```
Load a language file.  Tries the current and default themes as well as the user and global languages.



Type|Parameter|Description
---|---|---
`string`|`$template_name`|The name of a template file
`string`|`$lang`|A specific language to load this file from
`bool`|`$fatal`|Whether to die with an error if it can't be loaded
`bool`|`$force_reload`|Whether to load the file again if it's already loaded

### getBoardParents

```php
function getBoardParents($id_parent)
```
Get all parent boards (requires first parent as parameter)
It finds all the parents of id_parent, and that board itself.

Additionally, it detects the moderators of said boards.

Type|Parameter|Description
---|---|---
`int`|`$id_parent`|The ID of the parent board

### getLanguages

```php
function getLanguages($use_cache = true)
```
Attempt to reload our known languages.

It will try to choose only utf8 or non-utf8 languages.

Type|Parameter|Description
---|---|---
`bool`|`$use_cache`|Whether or not to use the cache

### censorText

```php
function censorText(&$text, $force = false)
```
Replace all vulgar words with respective proper words. (substring or whole words..)
What this function does:
 - it censors the passed string.

- if the theme setting allow_no_censored is on, and the theme option
show_no_censored is enabled, does not censor, unless force is also set.
 - it caches the list of censored words to reduce parsing.

Type|Parameter|Description
---|---|---
`string`|`&$text`|The text to censor
`bool`|`$force`|Whether to censor the text regardless of settings

### template_include

```php
function template_include($filename, $once = false)
```
Load the template/language file using require
	- loads the template or language file specified by filename.

- uses eval unless disableTemplateEval is enabled.
- outputs a parse error if the file did not exist or contained errors.
- attempts to detect the error and line, and show detailed information.

Type|Parameter|Description
---|---|---
`string`|`$filename`|The name of the file to include
`bool`|`$once`|If true only includes the file once (like include_once)

### loadDatabase

```php
function loadDatabase()
```
Initialize a database connection.



### loadCacheAccelerator

```php
function loadCacheAccelerator($overrideCache = null, $fallbackSMF = true)
```
Try to load up a supported caching method. This is saved in $cacheAPI if we are not overriding it.



Type|Parameter|Description
---|---|---
`string`|`$overrideCache`|Try to use a different cache method other than that defined in $cache_accelerator.
`bool`|`$fallbackSMF`|Use the default SMF method if the accelerator fails.

### cache_quick_get

```php
function cache_quick_get($key, $file, $function, $params, $level = 1)
```
Try to retrieve a cache entry. On failure, call the appropriate function.



Type|Parameter|Description
---|---|---
`string`|`$key`|The key for this entry
`string`|`$file`|The file associated with this entry
`string`|`$function`|The function to call
`array`|`$params`|Parameters to be passed to the specified function
`int`|`$level`|The cache level

### cache_put_data

```php
function cache_put_data($key, $value, $ttl = 120)
```
Puts value in the cache under key for ttl seconds.

- It may "miss" so shouldn't be depended on
- Uses the cache engine chosen in the ACP and saved in settings.php
- It supports:
 Xcache: https://xcache.lighttpd.net/wiki/XcacheApi
 memcache: https://php.net/memcache
 APC: https://php.net/apc
  APCu: https://php.net/book.apcu
 Zend: http://files.zend.com/help/Zend-Platform/output_cache_functions.htm
 Zend: http://files.zend.com/help/Zend-Platform/zend_cache_functions.htm

Type|Parameter|Description
---|---|---
`string`|`$key`|A key for this value
`mixed`|`$value`|The data to cache
`int`|`$ttl`|How long (in seconds) the data should be cached for

### cache_get_data

```php
function cache_get_data($key, $ttl = 120)
```
Gets the value from the cache specified by key, so long as it is not older than ttl seconds.

- It may often "miss", so shouldn't be depended on.
- It supports the same as cache_put_data().

Type|Parameter|Description
---|---|---
`string`|`$key`|The key for the value to retrieve
`int`|`$ttl`|The maximum age of the cached data

### clean_cache

```php
function clean_cache($type = '')
```
Empty out the cache in use as best it can

It may only remove the files of a certain type (if the $type parameter is given)
Type can be user, data or left blank
	- user clears out user data
 - data clears out system / opcode data
 - If no type is specified will perform a complete cache clearing
For cache engines that do not distinguish on types, a full cache flush will be done

Type|Parameter|Description
---|---|---
`string`|`$type`|The cache type ('memcached', 'apc', 'xcache', 'zend' or something else for SMF's file cache)

### set_avatar_data

```php
function set_avatar_data($data = array())
```
Helper function to set an array of data for an user's avatar.

Makes assumptions based on the data provided, the following keys are required:
- avatar The raw "avatar" column in members table
- email The user's email. Used to get the gravatar info
- filename The attachment filename

Type|Parameter|Description
---|---|---
`array`|`$data`|An array of raw info

### get_auth_secret

```php
function get_auth_secret()
```
Gets, and if necessary creates, the authentication secret to use for cookies, tokens, etc.

Note: Never use the $auth_secret variable directly. Always call this function instead.

