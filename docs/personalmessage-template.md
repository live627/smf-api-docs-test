---
layout: default
group: func
navtitle: PersonalMessage.template.php
title: ./Themes/default/PersonalMessage.template.php
count: 17
---
* auto-gen TOC:
{:toc}
### template_pm_above

```php
function template_pm_above(): void
```
This is for stuff above the menu in the personal messages section



### template_pm_below

```php
function template_pm_below(): void
```
Just the end of the index bar, nothing special.



### template_pm_popup

```php
function template_pm_popup(): void
```
Displays a popup with information about your personal messages



### template_folder

```php
function template_folder(): void
```
Shows a particular folder (eg inbox or outbox), all the PMs in it, etc.



### template_single_pm

```php
function template_single_pm(array $message): void
```
Template for displaying a single personal message.



Type|Parameter|Description
---|---|---
`array`|`$message`|An array of information about the message to display\.

### template_subject_list

```php
function template_subject_list(): void
```
Just list all the personal message subjects - to make templates easier.



### template_search

```php
function template_search(): void
```
The form for the PM search feature



### template_search_results

```php
function template_search_results(): void
```
Displays results from a PM search



### template_send

```php
function template_send(): void
```
The form for sending a new PM



### template_ask_delete

```php
function template_ask_delete(): void
```
This template asks the user whether they wish to empty out their folder/messages.



### template_prune

```php
function template_prune(): void
```
This template asks the user what messages they want to prune.



### template_labels

```php
function template_labels(): void
```
Here we allow the user to setup labels, remove labels and change rules for labels (i.e, do quite a bit)



### template_report_message

```php
function template_report_message(): void
```
Template for reporting a personal message.



### template_report_message_complete

```php
function template_report_message_complete(): void
```
Little template just to say "Yep, it's been submitted"



### template_rules

```php
function template_rules(): void
```
Manage rules.



### template_add_rule

```php
function template_add_rule(): void
```
Template for adding/editing a rule.



### template_showPMDrafts

```php
function template_showPMDrafts(): void
```
Template for showing all of a user's PM drafts.



