---
layout: default
group: func
navtitle: Subs.php
title: ./Sources/Subs.php
count: 87
---
* auto-gen TOC:
{:toc}
### updateStats

```php
function updateStats(string $type, mixed $parameter1 = null, mixed $parameter2 = null): void
```
Update some basic statistics.

'member' statistic updates the latest member, the total member
 count, and the number of unapproved members.
'member' also only counts approved members when approval is on, but
 is much more efficient with it off.

'message' changes the total number of messages, and the
 highest message id by id_msg - which can be parameters 1 and 2,
 respectively.

'topic' updates the total number of topics, or if parameter1 is true
 simply increments them.

'subject' updates the log_search_subjects in the event of a topic being
 moved, removed or split.  parameter1 is the topicid, parameter2 is the new subject

'postgroups' case updates those members who match condition's
 post-based membergroups in the database (restricted by parameter1).

Type|Parameter|Description
---|---|---
`string`|`$type`|Stat type - can be 'member', 'message', 'topic', 'subject' or 'postgroups'
`mixed`|`$parameter1`|A parameter for updating the stats
`mixed`|`$parameter2`|A 2nd parameter for updating the stats

### updateMemberData

```php
function updateMemberData(mixed $members, array $data): void
```
Updates the columns in the members table.

Assumes the data has been htmlspecialchar'd.
this function should be used whenever member data needs to be
updated in place of an UPDATE query.

id_member is either an int or an array of ints to be updated.

data is an associative array of the columns to be updated and their respective values.
any string values updated should be quoted and slashed.

the value of any column can be '+' or '-', which mean 'increment'
and decrement, respectively.

if the member's post number is updated, updates their post groups.

Type|Parameter|Description
---|---|---
`mixed`|`$members`|An array of member IDs, the ID of a single member, or null to update this for all members
`array`|`$data`|The info to update for the members

Integration hooks
: integrate_change_member_data

### updateSettings

```php
function updateSettings(array $changeArray, bool $update = false): void
```
Updates the settings table as well as $modSettings... only does one at a time if $update is true.

- updates both the settings table and $modSettings array.
- all of changeArray's indexes and values are assumed to have escaped apostrophes (')!
- if a variable is already set to what you want to change it to, that
  variable will be skipped over; it would be unnecessary to reset.
- When use_update is true, UPDATEs will be used instead of REPLACE.
- when use_update is true, the value can be true or false to increment
 or decrement it, respectively.

Type|Parameter|Description
---|---|---
`array`|`$changeArray`|An array of info about what we're changing in 'setting' => 'value' format
`bool`|`$update`|Whether to use an UPDATE query instead of a REPLACE query

### constructPageIndex

```php
function constructPageIndex(string $base_url, int &$start, int $max_value, int $num_per_page, bool $flexible_start = false, bool $show_prevnext = true): string
```
Constructs a page list.

- builds the page list, e.g. 1 ... 6 7 [8] 9 10 ... 15.
- flexible_start causes it to use "url.page" instead of "url;start=page".
- very importantly, cleans up the start value passed, and forces it to
  be a multiple of num_per_page.
- checks that start is not more than max_value.
- base_url should be the URL without any start parameter on it.
- uses the compactTopicPagesEnable and compactTopicPagesContiguous
  settings to decide how to display the menu.

an example is available near the function definition.
$pageindex = constructPageIndex($scripturl . '?board=' . $board, $_REQUEST['start'], $num_messages, $maxindex, true);

Type|Parameter|Description
---|---|---
`string`|`$base_url`|The basic URL to be used for each link.
`int`|` &$start`|The start position, by reference. If this is not a multiple of the number of items per page, it is sanitized to be so and the value will persist upon the function's return.
`int`|`$max_value`|The total number of items you are paginating for.
`int`|`$num_per_page`|The number of items to be displayed on a given page. $start will be forced to be a multiple of this value.
`bool`|`$flexible_start`|Whether a ;start=x component should be introduced into the URL automatically (see above)
`bool`|`$show_prevnext`|Whether the Previous and Next links should be shown (should be on only when navigating the list)

### comma_format

```php
function comma_format(float $number, bool|int $override_decimal_count = false): string
```
- Formats a number.

- uses the format of number_format to decide how to format the number.
  for example, it might display "1 234,50".
- caches the formatting data from the setting for optimization.

Type|Parameter|Description
---|---|---
`float`|`$number`|A number
`bool`&#124;`int`|`$override_decimal_count`|If set, will use the specified number of decimal places. Otherwise it's automatically determined

### timeformat

```php
function timeformat(int $log_time, bool|string $show_today = true, ?string $tzid = null): string
```
Format a time to make it look purdy.

- returns a pretty formatted version of time based on the user's format in $user_info['time_format'].
- applies all necessary time offsets to the timestamp, unless offset_type is set.
- if todayMod is set and show_today was not not specified or true, an
  alternate format string is used to show the date with something to show it is "today" or "yesterday".
- performs localization (more than just strftime would do alone.)

Type|Parameter|Description
---|---|---
`int`|`$log_time`|A timestamp
`bool`&#124;`string`|`$show_today`|Whether to show "Today"/"Yesterday" or just a date.
If a string is specified, that is used to temporarily override the date format.
`null`&#124;`string`|`$tzid`|Time zone to use when generating the formatted string.
If empty, the user's time zone will be used.
If set to 'forum', the value of $modSettings['default_timezone'] will be used.
If set to a valid time zone identifier, that will be used.
Otherwise, the value of date_default_timezone_get() will be used.

### get_date_or_time_format

```php
function get_date_or_time_format(string $type = '', string $format = ''): string
```
Gets a version of a strftime() format that only shows the date or time components



Type|Parameter|Description
---|---|---
`string`|`$type`|Either 'date' or 'time'.
`string`|`$format`|A strftime() format to process. Defaults to $user_info['time_format'].

### smf_strftime

```php
function smf_strftime(string $format, ?int $timestamp = null, ?string $tzid = null): string
```
Replacement for strftime() that is compatible with PHP 8.1+.

This does not use the system's strftime library or locale setting,
so results may vary in a few cases from the results of strftime():

 - %a, %A, %b, %B, %p, %P: Output will use SMF's language strings
   to localize these values. If SMF's language strings have not
   been loaded, PHP's default English strings will be used.

 - %c, %x, %X: Output will always use ISO format.

Type|Parameter|Description
---|---|---
`string`|`$format`|A strftime() format string.
`int`&#124;`null`|`$timestamp`|A Unix timestamp.
If null, defaults to the current time.
`string`&#124;`null`|`$tzid`|Time zone identifier.
If null, uses default time zone.

### smf_gmstrftime

```php
function smf_gmstrftime(string $format, ?int $timestamp = null): string
```
Replacement for gmstrftime() that is compatible with PHP 8.1+.

Calls smf_strftime() with the $tzid parameter set to 'UTC'.

Type|Parameter|Description
---|---|---
`string`|`$format`|A strftime() format string.
`int`&#124;`null`|`$timestamp`|A Unix timestamp.
If null, defaults to the current time.

### un_htmlspecialchars

```php
function un_htmlspecialchars(string $string): string
```
Replaces special entities in strings with the real characters.

Functionally equivalent to htmlspecialchars_decode(), except that this also
replaces '&nbsp;' with a simple space character.

Type|Parameter|Description
---|---|---
`string`|`$string`|A string

### sanitize_chars

```php
function sanitize_chars(string $string, int $level = 0, ?string $substitute = null): string
```
Replaces invalid characters with a substitute.

!!! Warning !!! Setting $substitute to '' in order to delete invalid
characters from the string can create unexpected security problems. See
https://www.unicode.org/reports/tr36/#Deletion_of_Noncharacters for an
explanation.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string to sanitize.
`int`|`$level`|Controls filtering of invisible formatting characters.
0: Allow valid formatting characters. Use for sanitizing text in posts.
1: Allow necessary formatting characters. Use for sanitizing usernames.
2: Disallow all formatting characters. Use for internal comparisions
   only, such as in the word censor, search contexts, etc.
Default: 0.
`string`&#124;`null`|`$substitute`|Replacement string for the invalid characters.
If not set, the Unicode replacement character (U+FFFD) will be used
(or a fallback like "?" if necessary).

### normalize_spaces

```php
function normalize_spaces(string $string, bool $vspace = true, bool $hspace = false, array $options = array()): string
```
Normalizes space characters and line breaks.



Type|Parameter|Description
---|---|---
`string`|`$string`|The string to sanitize.
`bool`|`$vspace`|If true, replaces all line breaks and vertical space
characters with "\n". Default: true.
`bool`|`$hspace`|If true, replaces horizontal space characters with a
plain " " character. (Note: tabs are not replaced unless the
'replace_tabs' option is supplied.) Default: false.
`array`|`$options`|An array of boolean options. Possible values are:
- no_breaks: Vertical spaces are replaced by " " instead of "\n".
- replace_tabs: If true, tabs are are replaced by " " chars.
- collapse_hspace: If true, removes extra horizontal spaces.

### shorten_subject

```php
function shorten_subject(string $subject, int $len): string
```
Shorten a subject + internationalization concerns.

- shortens a subject so that it is either shorter than length, or that length plus an ellipsis.
- respects internationalization characters and entities as one character.
- avoids trailing entities.
- returns the shortened string.

Type|Parameter|Description
---|---|---
`string`|`$subject`|The subject
`int`|`$len`|How many characters to limit it to

### forum_time

```php
function forum_time(bool $use_user_offset = true, int $timestamp = null): int
```
Deprecated function that formerly applied manual offsets to Unix timestamps
in order to provide a fake version of time zone support on ancient versions
of PHP. It now simply returns an unaltered timestamp.



Type|Parameter|Description
---|---|---
`bool`|`$use_user_offset`|This parameter is deprecated and nonfunctional
`int`|`$timestamp`|A timestamp (null to use current time)

### permute

```php
function permute(array $array): array
```
Calculates all the possible permutations (orders) of array.

should not be called on huge arrays (bigger than like 10 elements.)
returns an array containing each permutation.

Type|Parameter|Description
---|---|---
`array`|`$array`|An array

### get_signature_allowed_bbc_tags

```php
function get_signature_allowed_bbc_tags(): array
```
Return an array with allowed bbc tags for signatures, that can be passed to parse_bbc().



### parse_bbc

```php
function parse_bbc(string|bool $message, bool $smileys = true, string $cache_id = '', array $parse_tags = array()): string
```
Parse bulletin board code in a string, as well as smileys optionally.

- only parses bbc tags which are not disabled in disabledBBC.
- handles basic HTML, if enablePostHTML is on.
- caches the from/to replace regular expressions so as not to reload them every time a string is parsed.
- only parses smileys if smileys is true.
- does nothing if the enableBBC setting is off.
- uses the cache_id as a unique identifier to facilitate any caching it may do.
- returns the modified message.

Type|Parameter|Description
---|---|---
`string`&#124;`bool`|`$message`|The message.
When a empty string, nothing is done.
When false we provide a list of BBC codes available.
When a string, the message is parsed and bbc handled.
`bool`|`$smileys`|Whether to parse smileys as well
`string`|`$cache_id`|The cache ID
`array`|`$parse_tags`|If set, only parses these tags rather than all of them

Integration hooks
: integrate_pre_parsebbc
: integrate_attach_bbc_validate
: integrate_bbc_codes
: integrate_bbc_print
: integrate_autolinker_schemes
: integrate_post_parsebbc

### parsesmileys

```php
function parsesmileys(string &$message): void
```
Parse smileys in the passed message.

The smiley parsing function which makes pretty faces appear :).
If custom smiley sets are turned off by smiley_enable, the default set of smileys will be used.
These are specifically not parsed in code tags [url=mailto:Dad@blah.com]
Caches the smileys from the database or array in memory.
Doesn't return anything, but rather modifies message directly.

Type|Parameter|Description
---|---|---
`string`|` &$message`|The message to parse smileys in

Integration hooks
: integrate_smileys

### highlight_php_code

```php
function highlight_php_code(string $code): string
```
Highlight any code.

Uses PHP's highlight_string() to highlight PHP syntax
does special handling to keep the tabs in the code available.
used to parse PHP code from inside [code] and [php] tags.

Type|Parameter|Description
---|---|---
`string`|`$code`|The code

### get_proxied_url

```php
function get_proxied_url(string $url): string
```
Gets the appropriate URL to use for images (or whatever) when using SSL

The returned URL may or may not be a proxied URL, depending on the situation.
Mods can implement alternative proxies using the 'integrate_proxy' hook.

Type|Parameter|Description
---|---|---
`string`|`$url`|The original URL of the requested resource

Integration hooks
: integrate_proxy

### redirectexit

```php
function redirectexit(string $setLocation = '', bool $refresh = false, bool $permanent = false): void
```
Make sure the browser doesn't come back and repost the form data.

Should be used whenever anything is posted.

Type|Parameter|Description
---|---|---
`string`|`$setLocation`|The URL to redirect them to
`bool`|`$refresh`|Whether to use a meta refresh instead
`bool`|`$permanent`|Whether to send a 301 Moved Permanently instead of a 302 Moved Temporarily

Integration hooks
: integrate_redirect

### obExit

```php
function obExit(bool $header = null, bool $do_footer = null, bool $from_index = false, bool $from_fatal_error = false): void
```
Ends execution.  Takes care of template loading and remembering the previous URL.



Type|Parameter|Description
---|---|---
`bool`|`$header`|Whether to do the header
`bool`|`$do_footer`|Whether to do the footer
`bool`|`$from_index`|Whether we're coming from the board index
`bool`|`$from_fatal_error`|Whether we're coming from a fatal error

Integration hooks
: integrate_exit

### url_image_size

```php
function url_image_size(string $url): array|false
```
Get the size of a specified image with better error handling.



Type|Parameter|Description
---|---|---
`string`|`$url`|The URL of the image

### setupThemeContext

```php
function setupThemeContext(bool $forceload = false): void
```
Sets up the basic theme context stuff.



Type|Parameter|Description
---|---|---
`bool`|`$forceload`|Whether to load the theme even if it's already loaded

Integration hooks
: integrate_theme_context

### setMemoryLimit

```php
function setMemoryLimit(string $needed, bool $in_use = false): bool
```
Helper function to set the system memory to a needed value
- If the needed memory is greater than current, will attempt to get more
- if in_use is set to true, will also try to take the current memory usage in to account



Type|Parameter|Description
---|---|---
`string`|`$needed`|The amount of memory to request, if needed, like 256M
`bool`|`$in_use`|Set to true to account for current memory usage of the script

### memoryReturnBytes

```php
function memoryReturnBytes(string $val): int
```
Helper function to convert memory string settings to bytes



Type|Parameter|Description
---|---|---
`string`|`$val`|The byte string, like 256M or 1G

### template_header

```php
function template_header(): void
```
The header template



Integration hooks
: integrate_security_files

### theme_copyright

```php
function theme_copyright(): void
```
Show the copyright.



### template_footer

```php
function template_footer(): void
```
The template footer



### template_javascript

```php
function template_javascript(bool $do_deferred = false): void
```
Output the Javascript files
	- tabbing in this function is to make the HTML source look good and proper
 - if deferred is set function will output all JS set to load at page end



Type|Parameter|Description
---|---|---
`bool`|`$do_deferred`|If true will only output the deferred JS (the stuff that goes right before the closing body tag)

Integration hooks
: integrate_pre_javascript_output

### template_css

```php
function template_css(): void
```
Output the CSS files



Integration hooks
: integrate_pre_css_output

### custMinify

```php
function custMinify(array $data, string $type): array
```
Get an array of previously defined files and adds them to our main minified files.

Sets a one day cache to avoid re-creating a file on every request.

Type|Parameter|Description
---|---|---
`array`|`$data`|The files to minify.
`string`|`$type`|either css or js.

### deleteAllMinified

```php
function deleteAllMinified(): void
```
Clears out old minimized CSS and JavaScript files and ensures $modSettings['browser_cache'] is up to date



### getAttachmentFilename

```php
function getAttachmentFilename(string $filename, int $attachment_id, ?string $dir = null, bool $new = false, string $file_hash = ''): string
```
Get an attachment's encrypted filename. If $new is true, won't check for file existence.



Type|Parameter|Description
---|---|---
`string`|`$filename`|The name of the file
`int`|`$attachment_id`|The ID of the attachment
`string`&#124;`null`|`$dir`|Which directory it should be in (null to use current one)
`bool`|`$new`|Whether this is a new attachment
`string`|`$file_hash`|The file hash

### ip2range

```php
function ip2range(string $fullip): array
```
Convert a single IP to a ranged IP.

internal function used to convert a user-readable format to a format suitable for the database.

Type|Parameter|Description
---|---|---
`string`|`$fullip`|The full IP

### host_from_ip

```php
function host_from_ip(string $ip): string
```
Lookup an IP; try shell_exec first because we can do a timeout on it.



Type|Parameter|Description
---|---|---
`string`|`$ip`|The IP to get the hostname from

### text2words

```php
function text2words(string $text, int $max_chars = 20, bool $encrypt = false): array
```
Chops a string into words and prepares them to be inserted into (or searched from) the database.



Type|Parameter|Description
---|---|---
`string`|`$text`|The text to split into words
`int`|`$max_chars`|The maximum number of characters per word
`bool`|`$encrypt`|Whether to encrypt the results

### create_button

```php
function create_button(string $name, string $alt, string $label = '', string $custom = '', bool $force_use = false): string
```
Creates an image/text button



Type|Parameter|Description
---|---|---
`string`|`$name`|The name of the button (should be a main_icons class or the name of an image)
`string`|`$alt`|The alt text
`string`|`$label`|The $txt string to use as the label
`string`|`$custom`|Custom text/html to add to the img tag (only when using an actual image)
`bool`|`$force_use`|Whether to force use of this when template_create_button is available

### setupMenuContext

```php
function setupMenuContext(): void
```
Sets up all of the top menu buttons
Saves them in the cache if it is available and on
Places the results in $context



Integration hooks
: integrate_menu_buttons
: integrate_current_action

### smf_seed_generator

```php
function smf_seed_generator(): void
```
Generate a random seed and ensure it's stored in settings.



### call_integration_hook

```php
function call_integration_hook(string $hook, array $parameters = array()): array
```
Process functions of an integration hook.

calls all functions of the given hook.
supports static class method calls.

Type|Parameter|Description
---|---|---
`string`|`$hook`|The hook name
`array`|`$parameters`|An array of parameters this hook implements

### add_integration_function

```php
function add_integration_function(string $hook, string $function, bool $permanent = true, string $file = '', bool $object = false): void
```
Add a function for integration hook.

does nothing if the function is already added.

Type|Parameter|Description
---|---|---
`string`|`$hook`|The complete hook name.
`string`|`$function`|The function name. Can be a call to a method via Class::method.
`bool`|`$permanent`|If true, updates the value in settings table.
`string`|`$file`|The file. Must include one of the following wildcards: $boarddir, $sourcedir, $themedir, example: $sourcedir/Test.php
`bool`|`$object`|Indicates if your class will be instantiated when its respective hook is called. If true, your function must be a method.

### remove_integration_function

```php
function remove_integration_function(string $hook, string $function, bool $permanent = true, string $file = '', bool $object = false): void
```
Remove an integration hook function.

Removes the given function from the given hook.
Does nothing if the function is not available.

Type|Parameter|Description
---|---|---
`string`|`$hook`|The complete hook name.
`string`|`$function`|The function name. Can be a call to a method via Class::method.
`bool`|`$permanent`|Irrelevant for the function itself but need to declare it to match
`string`|`$file`|The filename. Must include one of the following wildcards: $boarddir, $sourcedir, $themedir, example: $sourcedir/Test.php
`bool`|`$object`|Indicates if your class will be instantiated when its respective hook is called. If true, your function must be a method.

### call_helper

```php
function call_helper(mixed $string, bool $return = false): string|array|bool
```
Receives a string and tries to figure it out if its a method or a function.

If a method is found, it looks for a "#" which indicates SMF should create a new instance of the given class.
Checks the string/array for is_callable() and return false/fatal_lang_error is the given value results in a non callable string/array.
Prepare and returns a callable depending on the type of method/function found.

Type|Parameter|Description
---|---|---
`mixed`|`$string`|The string containing a function name or a static call. The function can also accept a closure, object or a callable array (object/class, valid_callable)
`bool`|`$return`|If true, the function will not call the function/method but instead will return the formatted string.

### load_file

```php
function load_file(string $string): string|bool
```
Receives a string and tries to figure it out if it contains info to load a file.

Checks for a | (pipe) symbol and tries to load a file with the info given.
The string should be format as follows File.php|. You can use the following wildcards: $boarddir, $sourcedir and if available at the moment of execution, $themedir.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string containing a valid format.

### fetch_web_data

```php
function fetch_web_data(string $url, string $post_data = '', bool $keep_alive = false, int $redirection_level = 0): string|false
```
Get the contents of a URL, irrespective of allow_url_fopen.

- reads the contents of an http or ftp address and returns the page in a string
- will accept up to 3 page redirections (redirectio_level in the function call is private)
- if post_data is supplied, the value and length is posted to the given url as form data
- URL must be supplied in lowercase

Type|Parameter|Description
---|---|---
`string`|`$url`|The URL
`string`|`$post_data`|The data to post to the given URL
`bool`|`$keep_alive`|Whether to send keepalive info
`int`|`$redirection_level`|How many levels of redirection

### get_mime_type

```php
function get_mime_type(string $data, string $is_path = false): string|bool
```
Attempts to determine the MIME type of some data or a file.



Type|Parameter|Description
---|---|---
`string`|`$data`|The data to check, or the path or URL of a file to check.
`string`|`$is_path`|If true, $data is a path or URL to a file.

### check_mime_type

```php
function check_mime_type(string $data, string $type_pattern, string $is_path = false): int
```
Checks whether a file or data has the expected MIME type.



Type|Parameter|Description
---|---|---
`string`|`$data`|The data to check, or the path or URL of a file to check.
`string`|`$type_pattern`|A regex pattern to match the acceptable MIME types.
`string`|`$is_path`|If true, $data is a path or URL to a file.

### prepareLikesContext

```php
function prepareLikesContext(int $topic): array
```
Prepares an array of "likes" info for the topic specified by $topic



Type|Parameter|Description
---|---|---
`int`|`$topic`|The topic ID to fetch the info from.

### sanitizeMSCutPaste

```php
function sanitizeMSCutPaste(string $string): string
```
Microsoft uses their own character set Code Page 1252 (CP1252), which is a
superset of ISO 8859-1, defining several characters between DEC 128 and 159
that are not normally displayable.  This converts the popular ones that
appear from a cut and paste from windows.



Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### replaceEntities__callback

```php
function replaceEntities__callback(array $matches): string
```
Decode numeric html entities to their ascii or UTF8 equivalent character.

Callback function for preg_replace_callback in subs-members
Uses capture group 2 in the supplied array
Does basic scan to ensure characters are inside a valid range

Type|Parameter|Description
---|---|---
`array`|`$matches`|An array of matches (relevant info should be the 3rd item)

### fixchar__callback

```php
function fixchar__callback(array $matches): string
```
Converts html entities to utf8 equivalents

Callback function for preg_replace_callback
Uses capture group 1 in the supplied array
Does basic checks to keep characters inside a viewable range.

Type|Parameter|Description
---|---|---
`array`|`$matches`|An array of matches (relevant info should be the 2nd item in the array)

### entity_fix__callback

```php
function entity_fix__callback(array $matches): string
```
Strips out invalid html entities, replaces others with html style &#123; codes

Callback function used of preg_replace_callback in smcFunc $ent_checks, for example
strpos, strlen, substr etc

Type|Parameter|Description
---|---|---
`array`|`$matches`|An array of matches (relevant info should be the 3rd item in the array)

### get_gravatar_url

```php
function get_gravatar_url(string $email_address): string
```
Return a Gravatar URL based on
- the supplied email address,
- the global maximum rating,
- the global default fallback,
- maximum sizes as set in the admin panel.

It is SSL aware, and caches most of the parameters.

Type|Parameter|Description
---|---|---
`string`|`$email_address`|The user's email address

### smf_list_timezones

```php
function smf_list_timezones(string $when = 'now'): array
```
Get a list of time zones.



Type|Parameter|Description
---|---|---
`string`|`$when`|The date/time for which to calculate the time zone values.
May be a Unix timestamp or any string that strtotime() can understand.
Defaults to 'now'.

### getUserTimezone

```php
function getUserTimezone(int $id_member = null): string
```
Gets a member's selected time zone identifier



Type|Parameter|Description
---|---|---
`int`|`$id_member`|The member id to look up. If not provided, the current user's id will be used.

### inet_ptod

```php
function inet_ptod(string $ip_address): string|false
```
Converts an IP address into binary



Type|Parameter|Description
---|---|---
`string`|`$ip_address`|An IP address in IPv4, IPv6 or decimal notation

### inet_dtop

```php
function inet_dtop(string $bin): string|false
```
Converts a binary version of an IP address into a readable format



Type|Parameter|Description
---|---|---
`string`|`$bin`|An IP address in IPv4, IPv6 (Either string (postgresql) or binary (other databases))

### _safe_serialize

```php
function _safe_serialize(mixed $value): string
```
Safe serialize() replacement. Recursive
- output a strict subset of PHP's native serialized representation
- does not serialize objects



Type|Parameter|Description
---|---|---
`mixed`|`$value`|

### safe_serialize

```php
function safe_serialize(mixed $value): string
```
Wrapper for _safe_serialize() that handles exceptions and multibyte encoding issues.



Type|Parameter|Description
---|---|---
`mixed`|`$value`|

### _safe_unserialize

```php
function _safe_unserialize(string $str): mixed
```
Safe unserialize() replacement
- accepts a strict subset of PHP's native serialized representation
- does not unserialize objects



Type|Parameter|Description
---|---|---
`string`|`$str`|

### safe_unserialize

```php
function safe_unserialize(string $str): mixed
```
Wrapper for _safe_unserialize() that handles exceptions and multibyte encoding issue



Type|Parameter|Description
---|---|---
`string`|`$str`|

### smf_chmod

```php
function smf_chmod(string $file, int $value = 0): bool
```
Tries different modes to make file/dirs writable. Wrapper function for chmod()



Type|Parameter|Description
---|---|---
`string`|`$file`|The file/dir full path.
`int`|`$value`|Not needed, added for legacy reasons.

### smf_json_decode

```php
function smf_json_decode(string $json, bool $returnAsArray = false, bool $logIt = true): array
```
Wrapper function for json_decode() with error handling.



Type|Parameter|Description
---|---|---
`string`|`$json`|The string to decode.
`bool`|`$returnAsArray`|To return the decoded string as an array or an object, SMF only uses Arrays but to keep on compatibility with json_decode its set to false as default.
`bool`|`$logIt`|To specify if the error will be logged if theres any.

### isValidIP

```php
function isValidIP(string $IPString): bool
```
Check the given String if he is a valid IPv4 or IPv6
return true or false



Type|Parameter|Description
---|---|---
`string`|`$IPString`|

### smf_serverResponse

```php
function smf_serverResponse(string $data = '', string $type = 'content-type: application/json'): void
```
Outputs a response.

It assumes the data is already a string.

Type|Parameter|Description
---|---|---
`string`|`$data`|The data to print
`string`|`$type`|The content type. Defaults to Json.

### set_tld_regex

```php
function set_tld_regex(bool $update = false): void
```
Creates an optimized regex to match all known top level domains.

The optimized regex is stored in $modSettings['tld_regex'].

To update the stored version of the regex to use the latest list of valid
TLDs from iana.org, set the $update parameter to true. Updating can take some
time, based on network connectivity, so it should normally only be done by
calling this function from a background or scheduled task.

If $update is not true, but the regex is missing or invalid, the regex will
be regenerated from a hard-coded list of TLDs. This regenerated regex will be
overwritten on the next scheduled update.

Type|Parameter|Description
---|---|---
`bool`|`$update`|If true, fetch and process the latest official list of TLDs from iana.org.

### build_regex

```php
function build_regex(array $strings, string $delim = null, bool $returnArray = false): string|array
```
Creates optimized regular expressions from an array of strings.

An optimized regex built using this function will be much faster than a
simple regex built using `implode('|', $strings)` --- anywhere from several
times to several orders of magnitude faster.

However, the time required to build the optimized regex is approximately
equal to the time it takes to execute the simple regex. Therefore, it is only
worth calling this function if the resulting regex will be used more than
once.

Because PHP places an upper limit on the allowed length of a regex, very
large arrays of $strings may not fit in a single regex. Normally, the excess
strings will simply be dropped. However, if the $returnArray parameter is set
to true, this function will build as many regexes as necessary to accommodate
everything in $strings and return them in an array. You will need to iterate
through all elements of the returned array in order to test all possible
matches.

Type|Parameter|Description
---|---|---
`array`|`$strings`|An array of strings to make a regex for.
`string`|`$delim`|An optional delimiter character to pass to preg_quote().
`bool`|`$returnArray`|If true, returns an array of regexes.

### ssl_cert_found

```php
function ssl_cert_found(string $url): void
```
Check if the passed url has an SSL certificate.

Returns true if a cert was found & false if not.

Type|Parameter|Description
---|---|---
`string`|`$url`|to check, in $boardurl format (no trailing slash).

### https_redirect_active

```php
function https_redirect_active(string $url): void
```
Check if the passed url has a redirect to https:// by querying headers.

Returns true if a redirect was found & false if not.
Note that when force_ssl = 2, SMF issues its own redirect...  So if this
returns true, it may be caused by SMF, not necessarily an .htaccess redirect.

Type|Parameter|Description
---|---|---
`string`|`$url`|to check, in $boardurl format (no trailing slash).

### build_query_board

```php
function build_query_board(int $userid): void
```
Build query_wanna_see_board and query_see_board for a userid

Returns array with keys query_wanna_see_board and query_see_board

Type|Parameter|Description
---|---|---
`int`|`$userid`|of the user

### httpsOn

```php
function httpsOn(): bool
```
Check if the connection is using https.



### parse_iri

```php
function parse_iri(string $iri, int $component = -1): mixed
```
A wrapper for `parse_url($url)` that can handle URLs with international
characters (a.k.a. IRIs)



Type|Parameter|Description
---|---|---
`string`|`$iri`|The IRI to parse.
`int`|`$component`|Optional parameter to pass to parse_url().

### validate_iri

```php
function validate_iri(string $iri, int $flags = 0): string|bool
```
A wrapper for `filter_var($url, FILTER_VALIDATE_URL)` that can handle URLs
with international characters (a.k.a. IRIs)



Type|Parameter|Description
---|---|---
`string`|`$iri`|The IRI to test.
`int`|`$flags`|Optional flags to pass to filter_var()

### sanitize_iri

```php
function sanitize_iri(string $iri): string|bool
```
A wrapper for `filter_var($url, FILTER_SANITIZE_URL)` that can handle URLs
with international characters (a.k.a. IRIs)

Note: The returned value will still be an IRI, not a URL. To convert to URL,
feed the result of this function to iri_to_url()

Type|Parameter|Description
---|---|---
`string`|`$iri`|The IRI to sanitize.

### normalize_iri

```php
function normalize_iri(string $iri): string|bool
```
Performs Unicode normalization on IRIs.

Internally calls sanitize_iri(), then performs Unicode normalization on the
IRI as a whole, using NFKC normalization for the domain name (see RFC 3491)
and NFC normalization for the rest.

Type|Parameter|Description
---|---|---
`string`|`$iri`|The IRI to normalize.

### iri_to_url

```php
function iri_to_url(string $iri): string|bool
```
Converts a URL with international characters (an IRI) into a pure ASCII URL

Uses Punycode to encode any non-ASCII characters in the domain name, and uses
standard URL encoding on the rest.

Type|Parameter|Description
---|---|---
`string`|`$iri`|A IRI that may or may not contain non-ASCII characters.

### url_to_iri

```php
function url_to_iri(string $url): string|bool
```
Decodes a URL containing encoded international characters to UTF-8

Decodes any Punycode encoded characters in the domain name, then uses
standard URL decoding on the rest.

Type|Parameter|Description
---|---|---
`string`|`$url`|The pure ASCII version of a URL.

### check_cron

```php
function check_cron(): void
```
Ensures SMF's scheduled tasks are being run as intended

If the admin activated the cron_is_real_cron setting, but the cron job is
not running things at least once per day, we need to go back to SMF's default
behaviour using "web cron" JavaScript calls.

### send_http_status

```php
function send_http_status(int $code, string $status = ''): void
```
Sends an appropriate HTTP status header based on a given status code



Type|Parameter|Description
---|---|---
`int`|`$code`|The status code
`string`|`$status`|The string for the status. Set automatically if not provided.

### sentence_list

```php
function sentence_list(array $list): string
```
Concatenates an array of strings into a grammatically correct sentence list

Uses formats defined in the language files to build the list appropropriately
for the currently loaded language.

Type|Parameter|Description
---|---|---
`array`|`$list`|An array of strings to concatenate.

### truncate_array

```php
function truncate_array(array $array, int $max_length = 1900, int $deep = 3): array
```
Truncate an array to a specified length



Type|Parameter|Description
---|---|---
`array`|`$array`|The array to truncate
`int`|`$max_length`|The upperbound on the length
`int`|`$deep`|How levels in an multidimensional array should the function take into account.

### array_length

```php
function array_length(array $array, int $deep = 3): int
```
array_length Recursive



Type|Parameter|Description
---|---|---
`array`|`$array`|
`int`|`$deep`|How many levels should the function

### is_filtered_request

```php
function is_filtered_request(array $array, string $req_var): bool
```
Compares existance request variables against an array.

The input array is associative, where keys denote accepted values
in a request variable denoted by `$req_val`. Values can be:

- another associative array where at least one key must be found
  in the request and their values are accepted request values.
- A scalar value, in which case no furthur checks are done.

Type|Parameter|Description
---|---|---
`array`|`$array`|
`string`|`$req_var`|request variable

### cleanXml

```php
function cleanXml(string $string): string
```
Clean up the XML to make sure it doesn't contain invalid characters.

See https://www.w3.org/TR/xml/#charsets

Type|Parameter|Description
---|---|---
`string`|`$string`|The string to clean

### JavaScriptEscape

```php
function JavaScriptEscape(string $string, bool $as_json = false): string
```
Escapes (replaces) characters in strings to make them safe for use in JavaScript



Type|Parameter|Description
---|---|---
`string`|`$string`|The string to escape
`bool`|`$as_json`|If true, escape as double-quoted string. Default false.

### tokenTxtReplace

```php
function tokenTxtReplace($stringSubject = '')
```
