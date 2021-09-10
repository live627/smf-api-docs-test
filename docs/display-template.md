---
layout: default
group: func
navtitle: Display.template.php
title: ./Themes/default/Display.template.php
count: 3
---
* auto-gen TOC:
{:toc}
### template_main

```php
function template_main()
```
This template handles displaying a topic



### template_single_post

```php
function template_single_post($message)
```
Template for displaying a single post.



Type|Parameter|Description
---|---|---
`array`|`$message`|An array of information about the message to display. Should have 'id' and 'member'. Can also have 'first_new', 'is_ignored' and 'css_class'.

### template_quickreply

```php
function template_quickreply()
```
The template for displaying the quick reply box.



