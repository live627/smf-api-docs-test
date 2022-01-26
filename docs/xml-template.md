---
layout: default
group: func
navtitle: Xml.template.php
title: ./Themes/default/Xml.template.php
count: 19
---
* auto-gen TOC:
{:toc}
### template_sendbody

```php
function template_sendbody(): void
```
This defines the XML for sending the body of a message



### template_quotefast

```php
function template_quotefast(): void
```
This defines the XML for the AJAX quote feature



### template_modifyfast

```php
function template_modifyfast(): void
```
This defines the XML for the inline edit feature



### template_modifydone

```php
function template_modifydone(): void
```
The XML for handling things when you're done editing a post inline



### template_modifytopicdone

```php
function template_modifytopicdone(): void
```
This handles things when editing a topic's subject from the messageindex.



### template_post

```php
function template_post(): void
```
The massive XML for previewing posts.



### template_pm

```php
function template_pm(): void
```
All the XML for previewing a PM



### template_warning

```php
function template_warning(): void
```
The XML for previewing a warning



### template_stats

```php
function template_stats(): void
```
The XML for hiding/showing stats sections via AJAX



### template_split

```php
function template_split(): void
```
The XML for selecting items to split



### template_button_strip

```php
function template_button_strip($button_strip, $direction = 'top', $strip_options = array())
```
### template_menu

```php
function template_menu()
```
### theme_linktree

```php
function theme_linktree()
```
### template_results

```php
function template_results(): void
```
XML for search results



### template_jump_to

```php
function template_jump_to(): void
```
The XML for the Jump To box



### template_message_icons

```php
function template_message_icons(): void
```
The XML for displaying a column of message icons and selecting one via AJAX



### template_check_username

```php
function template_check_username(): void
```
The XML for instantly showing whether a username is valid on the registration page



### template_generic_xml

```php
function template_generic_xml(): void
```
This prints XML in its most generic form.



### template_generic_xml_recursive

```php
function template_generic_xml_recursive(array $xml_data, string $parent_ident, string $child_ident, int $level): void
```
Recursive function for displaying generic XML data.



Type|Parameter|Description
---|---|---
`array`|`$xml_data`|An array of XML data
`string`|`$parent_ident`|The parent tag
`string`|`$child_ident`|The child tag
`int`|`$level`|How many levels to indent the code

