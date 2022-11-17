---
layout: default
group: func
navtitle: BoardIndex.template.php
title: ./Themes/default/BoardIndex.template.php
count: 16
---
* auto-gen TOC:
{:toc}
### template_boardindex_outer_above

```php
function template_boardindex_outer_above(): void
```
The top part of the outer layer of the boardindex



### template_newsfader

```php
function template_newsfader(): void
```
This shows the newsfader



### template_main

```php
function template_main(): void
```
This actually displays the board index



### template_bi_board_icon

```php
function template_bi_board_icon(array $board): void
```
Outputs the board icon for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_bi_redirect_icon

```php
function template_bi_redirect_icon(array $board): void
```
Outputs the board icon for a redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_bi_board_info

```php
function template_bi_board_info(array $board): void
```
Outputs the board info for a standard board or redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_bi_board_stats

```php
function template_bi_board_stats(array $board): void
```
Outputs the board stats for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_bi_redirect_stats

```php
function template_bi_redirect_stats(array $board): void
```
Outputs the board stats for a redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_bi_board_lastpost

```php
function template_bi_board_lastpost(array $board): void
```
Outputs the board lastposts for a standard board or a redirect.

When on a mobile device, this may be hidden if no last post exists.

Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_bi_board_children

```php
function template_bi_board_children(array $board): void
```
Outputs the board children for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information\.

### template_boardindex_outer_below

```php
function template_boardindex_outer_below(): void
```
The lower part of the outer layer of the board index



### template_info_center

```php
function template_info_center(): void
```
Displays the info center



### template_ic_block_recent

```php
function template_ic_block_recent(): void
```
The recent posts section of the info center



### template_ic_block_calendar

```php
function template_ic_block_calendar(): void
```
The calendar section of the info center



### template_ic_block_stats

```php
function template_ic_block_stats(): void
```
The stats section of the info center



### template_ic_block_online

```php
function template_ic_block_online(): void
```
The who's online section of the info center



