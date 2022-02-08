---
layout: default
group: func
navtitle: QueryString.php
title: ./Sources/QueryString.php
count: 11
---
* auto-gen TOC:
{:toc}
### cleanRequest

```php
function cleanRequest(): void
```
Clean the request variables - add html entities to GET and slashes if magic_quotes_gpc is Off.

What it does:
- cleans the request variables (ENV, GET, POST, COOKIE, SERVER) and
- makes sure the query string was parsed correctly.
- handles the URLs passed by the queryless URLs option.
- makes sure, regardless of php.ini, everything has slashes.
- sets up $board, $topic, and $scripturl and $_REQUEST['start'].
- determines, or rather tries to determine, the client's IP.

### isValidIPv6

```php
function isValidIPv6(string $ip): bool
```
Validates a IPv6 address. returns true if it is ipv6.



Type|Parameter|Description
---|---|---
`string`|`$ip`|The ip address to be validated

### expandIPv6

```php
function expandIPv6(string $addr, bool $strict_check = true): string|bool
```
Expands a IPv6 address to its full form.



Type|Parameter|Description
---|---|---
`string`|`$addr`|The IPv6 address
`bool`|`$strict_check`|Whether to check the length of the expanded address for compliance

### matchIPtoCIDR

```php
function matchIPtoCIDR(string $ip_address, string $cidr_address): bool
```
Detect if a IP is in a CIDR address
- returns true or false



Type|Parameter|Description
---|---|---
`string`|`$ip_address`|IP address to check
`string`|`$cidr_address`|CIDR address to verify

### escapestring__recursive

```php
function escapestring__recursive(array|string $var): array|string
```
Adds slashes to the array/variable.

What it does:
- returns the var, as an array or string, with escapes as required.
- importantly escapes all keys and values!
- calls itself recursively if necessary.

Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$var`|A string or array of strings to escape

### htmlspecialchars__recursive

```php
function htmlspecialchars__recursive(array|string $var, int $level = 0): array|string
```
Adds html entities to the array/variable.  Uses two underscores to guard against overloading.

What it does:
- adds entities (&quot;, &lt;, &gt;) to the array or string var.
- importantly, does not effect keys, only values.
- calls itself recursively if necessary.

Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$var`|The string or array of strings to add entites to
`int`|`$level`|Which level we're at within the array (if called recursively)

### urldecode__recursive

```php
function urldecode__recursive(array|string $var, int $level = 0): array|string
```
Removes url stuff from the array/variable.  Uses two underscores to guard against overloading.

What it does:
- takes off url encoding (%20, etc.) from the array or string var.
- importantly, does it to keys too!
- calls itself recursively if there are any sub arrays.

Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$var`|The string or array of strings to decode
`int`|`$level`|Which level we're at within the array (if called recursively)

### unescapestring__recursive

```php
function unescapestring__recursive(array|string $var): array|string
```
Unescapes any array or variable.  Uses two underscores to guard against overloading.

What it does:
- unescapes, recursively, from the array or string var.
- effects both keys and values of arrays.
- calls itself recursively to handle arrays of arrays.

Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$var`|The string or array of strings to unescape

### stripslashes__recursive

```php
function stripslashes__recursive(array|string $var, int $level = 0): array|string
```
Remove slashes recursively.  Uses two underscores to guard against overloading.

What it does:
- removes slashes, recursively, from the array or string var.
- effects both keys and values of arrays.
- calls itself recursively to handle arrays of arrays.

Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$var`|The string or array of strings to strip slashes from
`int`|`$level`|= 0 What level we're at within the array (if called recursively)

### htmltrim__recursive

```php
function htmltrim__recursive(array|string $var, int $level = 0): array|string
```
Trim a string including the HTML space, character 160.  Uses two underscores to guard against overloading.

What it does:
- trims a string or an the var array using html characters as well.
- does not effect keys, only values.
- may call itself recursively if needed.

Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$var`|The string or array of strings to trim
`int`|`$level`|= 0 How deep we're at within the array (if called recursively)

### ob_sessrewrite

```php
function ob_sessrewrite(string $buffer): string
```
Rewrite URLs to include the session ID.

What it does:
- rewrites the URLs outputted to have the session ID, if the user
  is not accepting cookies and is using a standard web browser.
- handles rewriting URLs for the queryless URLs option.
- can be turned off entirely by setting $scripturl to an empty
  string, ''. (it wouldn't work well like that anyway.)
- because of bugs in certain builds of PHP, does not function in
  versions lower than 4.3.0 - please upgrade if this hurts you.

Type|Parameter|Description
---|---|---
`string`|`$buffer`|The unmodified output buffer

