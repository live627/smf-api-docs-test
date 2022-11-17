---
layout: default
group: func
navtitle: Subs-Compat.php
title: ./Sources/Subs-Compat.php
count: 12
---
* auto-gen TOC:
{:toc}
### sha1_smf

```php
function sha1_smf(string $str): string
```
Define the old SMF sha1 function. Uses mhash if available



Type|Parameter|Description
---|---|---
`string`|`$str`|The string

### sha1_core

```php
function sha1_core(string $x, int $len): string
```
This is the core SHA-1 calculation routine, used by sha1().



Type|Parameter|Description
---|---|---
`string`|`$x`|
`int`|`$len`|

### sha1_ft

```php
function sha1_ft(int $t, int $b, int $c, int $d): int
```
Helper function for the core SHA-1 calculation



Type|Parameter|Description
---|---|---
`int`|`$t`|
`int`|`$b`|
`int`|`$c`|
`int`|`$d`|

### sha1_kt

```php
function sha1_kt(int $t): int
```
Helper function for the core SHA-1 calculation



Type|Parameter|Description
---|---|---
`int`|`$t`|

### sha1_rol

```php
function sha1_rol(int $num, int $cnt): int
```
Helper function for the core SHA-1 calculation



Type|Parameter|Description
---|---|---
`int`|`$num`|
`int`|`$cnt`|

### sha1_raw

```php
function sha1_raw(string $text): string
```
Available since: (PHP 5)
If the optional raw_output is set to TRUE, then the sha1 digest is instead returned in raw binary format with a length of 20,
otherwise the returned value is a 40-character hexadecimal number.



Type|Parameter|Description
---|---|---
`string`|`$text`|The text to hash

### smf_crc32

```php
function smf_crc32(string $number): string
```
Compatibility function.

crc32 doesn't work as expected on 64-bit functions - make our own.
https://php.net/crc32#79567

Type|Parameter|Description
---|---|---
`string`|`$number`|

### mb_ord

```php
function mb_ord(string $string, ?string $encoding = null): int|bool
```
Compatibility function.

This is a complete polyfill.

Type|Parameter|Description
---|---|---
`string`|`$string`|A character.
`string`&#124;`null`|`$encoding`|The character encoding.
||If null, the current SMF encoding will be used, falling back to UTF-8.

### mb_chr

```php
function mb_chr(int $codepoint, ?string $encoding = null): string|bool
```
Compatibility function.

This is a complete polyfill.

Type|Parameter|Description
---|---|---
`int`|`$codepoint`|A Unicode codepoint value.
`string`&#124;`null`|`$encoding`|The character encoding.
||If null, the current SMF encoding will be used, falling back to UTF-8.

### mb_ord_chr_encoding

```php
function mb_ord_chr_encoding(string $encoding = null): string|bool
```
Helper function for the mb_ord and mb_chr polyfills.

Checks whether $encoding is a supported character encoding for the mb_ord
and mb_chr functions. If $encoding is null, the current default character
encoding is used. If the encoding is supported, it is returned as a string.
If not, false is returned.

Type|Parameter|Description
---|---|---
`string`|`$encoding`|A character encoding to check, or null for default.

### idn_to_ascii

```php
function idn_to_ascii(string $domain, int $flags = 0, int $variant = 1, ?array &$idna_info = null): string|bool
```
Compatibility function.

This is not a complete polyfill:

- $flags only supports IDNA_DEFAULT, IDNA_NONTRANSITIONAL_TO_ASCII,
  and IDNA_USE_STD3_RULES.
- $variant is ignored, because INTL_IDNA_VARIANT_UTS46 is always used.
- $idna_info is ignored.

Type|Parameter|Description
---|---|---
`string`|`$domain`|The domain to convert, which must be UTF-8 encoded.
`int`|`$flags`|A subset of possible IDNA_* flags.
`int`|`$variant`|Ignored in this compatibility function.
`array`&#124;`null`|`$idna_info`|Ignored in this compatibility function.

### idn_to_utf8

```php
function idn_to_utf8(string $domain, int $flags = 0, int $variant = 1, ?array &$idna_info = null): string|bool
```
Compatibility function.

This is not a complete polyfill:

- $flags only supports IDNA_DEFAULT, IDNA_NONTRANSITIONAL_TO_UNICODE,
  and IDNA_USE_STD3_RULES.
- $variant is ignored, because INTL_IDNA_VARIANT_UTS46 is always used.
- $idna_info is ignored.

Type|Parameter|Description
---|---|---
`string`|`$domain`|Domain to convert, in an IDNA ASCII-compatible format.
`int`|`$flags`|Ignored in this compatibility function.
`int`|`$variant`|Ignored in this compatibility function.
`array`&#124;`null`|`$idna_info`|Ignored in this compatibility function.

