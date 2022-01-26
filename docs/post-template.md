---
layout: default
group: func
navtitle: Post.template.php
title: ./Themes/default/Post.template.php
count: 6
---
* auto-gen TOC:
{:toc}
### template_main

```php
function template_main(): void
```
The main template for the post page.



### template_spellcheck

```php
function template_spellcheck(): void
```
The template for the spellchecker.



### template_quotefast

```php
function template_quotefast(): void
```
The template for the AJAX quote feature



### template_announce

```php
function template_announce(): void
```
The form for sending out an announcement



### template_announcement_send

```php
function template_announcement_send(): void
```
The confirmation/progress page, displayed after the admin has clicked the button to send the announcement.



### template_post_header

```php
function template_post_header(): void
```
Prints the input fields in the form's header (subject, message icon, guest name & email, etc.)

Mod authors can use the 'integrate_post_end' hook to modify or add to these (see Post.php).

Theme authors can customize the output in a couple different ways:
1. Change specific values in the $context['posting_fields'] array.
2. Add an 'html' element to the 'label' and/or 'input' elements of the field they want to
   change. This should contain the literal HTML string to be printed.

See the documentation in Post.php for more info on the $context['posting_fields'] array.

