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
function template_boardindex_outer_above()
```
The top part of the outer layer of the boardindex



### template_newsfader

```php
function template_newsfader()
```
This shows the newsfader



### template_main

```php
function template_main()
```
This actually displays the board index



### template_bi_board_icon

```php
function template_bi_board_icon($board)
```
Outputs the board icon for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_redirect_icon

```php
function template_bi_redirect_icon($board)
```
Outputs the board icon for a redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_info

```php
function template_bi_board_info($board)
```
Outputs the board info for a standard board or redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_stats

```php
function template_bi_board_stats($board)
```
Outputs the board stats for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_redirect_stats

```php
function template_bi_redirect_stats($board)
```
Outputs the board stats for a redirect.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_lastpost

```php
function template_bi_board_lastpost($board)
```
Outputs the board lastposts for a standard board or a redirect.

When on a mobile device, this may be hidden if no last post exists.

Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_bi_board_children

```php
function template_bi_board_children($board)
```
Outputs the board children for a standard board.



Type|Parameter|Description
---|---|---
`array`|`$board`|Current board information.

### template_boardindex_outer_below

```php
function template_boardindex_outer_below()
```
The lower part of the outer layer of the board index



### template_info_center

```php
function template_info_center()
```
Displays the info center



### template_ic_block_recent

```php
function template_ic_block_recent()
```
The recent posts section of the info center



### template_ic_block_calendar

```php
function template_ic_block_calendar()
```
The calendar section of the info center



### template_ic_block_stats

```php
function template_ic_block_stats()
```
The stats section of the info center



### template_ic_block_online

```php
function template_ic_block_online()
```
The who's online section of the admin center



