---
layout: default
group: func
navtitle: Subs-Charset.php
title: ./Sources/Subs-Charset.php
count: 11
---
* auto-gen TOC:
{:toc}
### utf8_strtolower

```php
function utf8_strtolower($string)
```
Converts the given UTF-8 string into lowercase.

Equivalent to mb_strtolower($string, 'UTF-8')

Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_strtoupper

```php
function utf8_strtoupper($string)
```
Convert the given UTF-8 string to uppercase.

Equivalent to mb_strtoupper($string, 'UTF-8')

Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_normalize_d

```php
function utf8_normalize_d($string)
```
Normalizes UTF-8 via Canonical Decomposition.



Type|Parameter|Description
---|---|---
`string`|`$string`|A UTF-8 string

### utf8_normalize_kd

```php
function utf8_normalize_kd($string)
```
Normalizes UTF-8 via Compatibility Decomposition.



Type|Parameter|Description
---|---|---
`string`|`$string`|A UTF-8 string.

### utf8_normalize_c

```php
function utf8_normalize_c($string)
```
Normalizes UTF-8 via Canonical Decomposition then Canonical Composition.



Type|Parameter|Description
---|---|---
`string`|`$string`|A UTF-8 string

### utf8_normalize_kc

```php
function utf8_normalize_kc($string)
```
Normalizes UTF-8 via Compatibility Decomposition then Canonical Composition.



Type|Parameter|Description
---|---|---
`string`|`$string`|The string

### utf8_compose

```php
function utf8_compose($string)
```
Helper function for utf8_normalize_c and utf8_normalize_kc



### utf8_normalize_d_maps

```php
function utf8_normalize_d_maps()
```
### utf8_normalize_kd_maps

```php
function utf8_normalize_kd_maps()
```
### utf8_compose_maps

```php
function utf8_compose_maps()
```
### utf8_combining_classes

```php
function utf8_combining_classes()
```
