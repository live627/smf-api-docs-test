---
layout: default
group: func
navtitle: RegularExpressions.php
title: ./Sources/Unicode/RegularExpressions.php
count: 4
---
* auto-gen TOC:
{:toc}
### utf8_regex_properties

```php
function utf8_regex_properties()
```
Helper function for utf8_sanitize_invisibles.

Character class lists compiled from:
https://unicode.org/Public/UNIDATA/DerivedCoreProperties.txt
https://unicode.org/Public/UNIDATA/PropList.txt
https://unicode.org/Public/UNIDATA/emoji/emoji-data.txt
https://unicode.org/Public/UNIDATA/extracted/DerivedGeneralCategory.txt

Developers: Do not update the data in this function manually. Instead,
run "php -f other/update_unicode_data.php" on the command line.

### utf8_regex_variation_selectors

```php
function utf8_regex_variation_selectors()
```
Helper function for utf8_sanitize_invisibles.

Character class lists compiled from:
https://unicode.org/Public/UNIDATA/StandardizedVariants.txt
https://unicode.org/Public/UNIDATA/emoji/emoji-variation-sequences.txt

Developers: Do not update the data in this function manually. Instead,
run "php -f other/update_unicode_data.php" on the command line.

### utf8_regex_joining_type

```php
function utf8_regex_joining_type()
```
Helper function for utf8_sanitize_invisibles.

Character class lists compiled from:
https://unicode.org/Public/UNIDATA/extracted/DerivedJoiningType.txt

Developers: Do not update the data in this function manually. Instead,
run "php -f other/update_unicode_data.php" on the command line.

### utf8_regex_indic

```php
function utf8_regex_indic()
```
Helper function for utf8_sanitize_invisibles.

Character class lists compiled from:
https://unicode.org/Public/UNIDATA/extracted/DerivedCombiningClass.txt
https://unicode.org/Public/UNIDATA/IndicSyllabicCategory.txt

Developers: Do not update the data in this function manually. Instead,
run "php -f other/update_unicode_data.php" on the command line.

