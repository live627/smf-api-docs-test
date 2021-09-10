---
layout: default
group: func
navtitle: ssi_examples.php
title: ./ssi_examples.php
count: 5
---
* auto-gen TOC:
{:toc}
### template_ssi_above

```php
function template_ssi_above()
```
Displays the header for this file



### template_ssi_below

```php
function template_ssi_below()
```
Displays the footer for this file



### template_homepage_sample1

```php
function template_homepage_sample1($method = 'source')
```
Displays a sample homepage to give you an idea of what's possible using SSI functions



Type|Parameter|Description
---|---|---
`string`|`$method`|If 'source', simply returns the source code, otherwise displays it

### template_homepage_sample1_php

```php
function template_homepage_sample1_php()
```
Generates the sample homepage. Used with template_homepage_sample1 if $method isn't 'source'.



### template_homepage_sample1_html

```php
function template_homepage_sample1_html()
```
Generates the HTML for the homepage sample. Used in conjunction with template_homepage_sample1 if method is 'source'



