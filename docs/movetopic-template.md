---
layout: default
group: func
navtitle: MoveTopic.template.php
title: ./Themes/default/MoveTopic.template.php
count: 5
---
* auto-gen TOC:
{:toc}
### template_move

```php
function template_move(): void
```
Show an interface for selecting which board to move a post to.



### template_redirect_options

```php
function template_redirect_options(string $type): void
```
Redirection topic options



Type|Parameter|Description
---|---|---
`string`|`$type`|What type of topic this is for - currently 'merge' or 'move'. Used to display appropriate text strings...

### template_merge_done

```php
function template_merge_done(): void
```
Confirmation page shown when finished merging topics.



### template_merge

```php
function template_merge(): void
```
Merge topic page.



### template_merge_extra_options

```php
function template_merge_extra_options(): void
```
Extra options related to merging topics.



