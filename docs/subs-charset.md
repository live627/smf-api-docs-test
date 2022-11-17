---
layout: default
group: func
navtitle: Subs-Charset.php
title: ./Sources/Subs-Charset.php
count: 12
---
* auto-gen TOC:
{:toc}
### utf8_strtolower

```php
function utf8_strtolower(string $string): string
```
Converts the given UTF-8 string into lowercase.

Equivalent to mb_strtolower($string, 'UTF-8'), except that we can keep the
output consistent across PHP versions and up to date with the latest version
of Unicode.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_strtoupper

```php
function utf8_strtoupper(string $string): string
```
Convert the given UTF-8 string to uppercase.

Equivalent to mb_strtoupper($string, 'UTF-8'), except that we can keep the
output consistent across PHP versions and up to date with the latest version
of Unicode.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_casefold

```php
function utf8_casefold(string $string): string
```
Casefolds the given UTF-8 string.

Equivalent to mb_convert_case($string, MB_CASE_FOLD, 'UTF-8'), except that
we can keep the output consistent across PHP versions and up to date with
the latest version of Unicode.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_convert_case

```php
function utf8_convert_case(string $string, string $case, bool $simple = false): string
```
Converts the case of the given UTF-8 string.



Type|Parameter|Description
---|---|---
`string`|`$string`|The string.
`string`|`$case`|One of 'upper', 'lower', 'fold', 'title', 'ucfirst', or 'ucwords'.
`bool`|`$simple`|If true, use simple maps instead of full maps. Default: false.

### utf8_normalize_d

```php
function utf8_normalize_d(string $string): string
```
Normalizes UTF-8 via Canonical Decomposition.



Type|Parameter|Description
---|---|---
`string`|`$string`|A UTF-8 string

### utf8_normalize_kd

```php
function utf8_normalize_kd(string $string): string
```
Normalizes UTF-8 via Compatibility Decomposition.



Type|Parameter|Description
---|---|---
`string`|`$string`|A UTF-8 string.

### utf8_normalize_c

```php
function utf8_normalize_c(string $string): string
```
Normalizes UTF-8 via Canonical Decomposition then Canonical Composition.



Type|Parameter|Description
---|---|---
`string`|`$string`|A UTF-8 string

### utf8_normalize_kc

```php
function utf8_normalize_kc(string $string): string
```
Normalizes UTF-8 via Compatibility Decomposition then Canonical Composition.



Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_normalize_kc_casefold

```php
function utf8_normalize_kc_casefold(string $string): string
```
Casefolds UTF-8 via Compatibility Composition Casefolding.

Used by idn_to_ascii polyfill in Subs-Compat.php

Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_decompose

```php
function utf8_decompose(array $chars, bool $compatibility = false): array
```
Helper function for utf8_normalize_d and utf8_normalize_kd.



Type|Parameter|Description
---|---|---
`array`|`$chars`|Array of Unicode characters
`bool`|`$compatibility`|If true, perform compatibility decomposition. Default false.

### utf8_compose

```php
function utf8_compose(array $chars): array
```
Helper function for utf8_normalize_c and utf8_normalize_kc.



Type|Parameter|Description
---|---|---
`array`|`$chars`|Array of decomposed Unicode characters

### utf8_sanitize_invisibles

```php
function utf8_sanitize_invisibles(string $string, int $level, string $substitute): string
```
Helper function for sanitize_chars() that deals with invisible characters.

This function deals with control characters, private use characters,
non-characters, and characters that are invisible by definition in the
Unicode standard. It does not deal with characters that are supposed to be
visible according to the Unicode standard, and makes no attempt to compensate
for possibly incomplete Unicode support in text rendering engines on client
devices.

Type|Parameter|Description
---|---|---
`string`|`$string`|The string to sanitize.
`int`|`$level`|Controls how invisible formatting characters are handled.
||0: Allow valid formatting characters. Use for sanitizing text in posts.
||1: Allow necessary formatting characters. Use for sanitizing usernames.
||2: Disallow all formatting characters. Use for internal comparisions
||   only, such as in the word censor, search contexts, etc.
`string`|`$substitute`|Replacement string for the invalid characters.

