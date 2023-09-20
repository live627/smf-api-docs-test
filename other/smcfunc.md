---
title: $smcFunc
group: themes
groupname: themes
---
* auto-gen TOC:
{:toc}
## String
These functions are defined in function reloadSettings, in Load.php. Some of these functions have the same name as standard PHP functions, but were designed to deal uniformly with UTF-8 character sets and HTML entities.
### `$smcFunc['entity_fix']` 
```php
function $smcFunc['entity_fix'](string $string): string
```
Strips out any control characters, byte order markers, and out of bounds Unicode characters. Replaces others with html style `&#123;` codes.

Type|Parameter|Description
---|---|---
`string`|`$string`|entity number; is hex if it starts wtith `x`

### `$smcFunc['htmlspecialchars']`

```php
function $smcFunc['entity_fix'](string $string, [int $quote_style = ENT_COMPAT, $charset = 'ISO-8859-1']): string
```
This function is similar to PHP's [`htmlspecialchars()`](http://php.net/htmlspecialchars) function; however, it additionally checks the encoding argument and takes care of HTML entities using regex.
### `$smcFunc['htmltrim']`
Like [`trim()`](http://php.net/trim), but it also trims off Unicode whitespacse off the beginning and the end of the string.
### `$smcFunc['strlen']`
Returns the character count of string, as an integer. 

The following entities are counted as one character:
- `&quot;`, `&amp;`, `&lt;`, `&gt;`, `&nbsp;`
- Any decimal entity in the form of `&$123456;`
### `$smcFunc['strpos']` 
### `$smcFunc['substr']`
Like [`substr()`](http://php.net/substr), but does not chop multibyte characters nor HTML entities.
### `$smcFunc['strtolower']` 
### `$smcFunc['strtoupper']` 
### `$smcFunc['ucfirst']`
### `$smcFunc['ucwords']`
### What's the difference between `$smcFunc['truncate']()` and `$smcFunc['substr']()`?

Both functions handle entities as single characters when counting. The difference is in how they interpret their `$length` arguments

A string may have entities in it. A simple `substr()` could easily end up cutting an entity (or even a multibyte character) in half, resulting in an invalid string. Calling `$smcFunc['truncate']()` will handle this correctly.

`$smcFunc['substr']()` produces a string that visually appears to be the specified length to a human reader. The real string length will be greater if the string contains any entities.

In contrast, `$smcFunc['truncate']()` produces a string whose real length will be equal to or less than the specified value. If the string contains any entities, it will visually appear to a human reader to be shorter than the specified length. This is great for when trying to ensure that the string fits into a database field that has a byte limit.
