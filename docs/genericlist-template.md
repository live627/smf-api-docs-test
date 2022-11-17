---
layout: default
group: func
navtitle: GenericList.template.php
title: ./Themes/default/GenericList.template.php
count: 2
---
* auto-gen TOC:
{:toc}
### template_show_list

```php
function template_show_list(string $list_id = null): void
```
This template handles displaying a list



Type|Parameter|Description
---|---|---
`string`|`$list_id`|The list ID\. If null, uses $context\['default\_list'\]\.

### template_additional_rows

```php
function template_additional_rows(string $row_position, array $cur_list): void
```
This template displays additional rows above or below the list.



Type|Parameter|Description
---|---|---
`string`|`$row_position`|The position \('top', 'bottom', etc\.\)
`array`|`$cur_list`|An array with the data for the current list

