---
layout: default
group: func
navtitle: MessageIndex.template.php
title: ./Themes/default/MessageIndex.template.php
count: 9
---
* auto-gen TOC:
{:toc}
### template_main

```php
function template_main(): void
```
The main messageindex.



### template_bi_board_icon

```php
function template_bi_board_icon(array $board): void
```
Outputs the board icon for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_redirect_icon

```php
function template_bi_redirect_icon(array $board): void
```
Outputs the board icon for a redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_info

```php
function template_bi_board_info(array $board): void
```
Outputs the board info for a standard board or redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_stats

```php
function template_bi_board_stats(array $board): void
```
Outputs the board stats for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_redirect_stats

```php
function template_bi_redirect_stats(array $board): void
```
Outputs the board stats for a redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_lastpost

```php
function template_bi_board_lastpost(array $board): void
```
Outputs the board lastposts for a standard board or a redirect.

When on a mobile device, this may be hidden if no last post exists.

Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_children

```php
function template_bi_board_children(array $board): void
```
Outputs the board children for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_topic_legend

```php
function template_topic_legend(): void
```
Shows a legend for topic icons.



