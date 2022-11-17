---
layout: default
group: func
navtitle: GenericControls.template.php
title: ./Themes/default/GenericControls.template.php
count: 3
---
* auto-gen TOC:
{:toc}
### template_control_richedit

```php
function template_control_richedit(string $editor_id, ?bool $smileyContainer = null, ?bool $bbcContainer = null): void
```
This function displays all the stuff you get with a richedit box - BBC, smileys, etc.



Type|Parameter|Description
---|---|---
`string`|`$editor_id`|The editor ID
`null` &#124; `bool`|`$smileyContainer`|If null, hides the smiley section regardless of settings
`null` &#124; `bool`|`$bbcContainer`|If null, hides the bbcode buttons regardless of settings

### template_control_richedit_buttons

```php
function template_control_richedit_buttons(string $editor_id): void
```
This template shows the form buttons at the bottom of the editor



Type|Parameter|Description
---|---|---
`string`|`$editor_id`|The editor ID

### template_control_verification

```php
function template_control_verification(int|string $verify_id, string $display_type = 'all', bool $reset = false): bool
```
This template displays a verification form



Type|Parameter|Description
---|---|---
`int` &#124; `string`|`$verify_id`|The verification control ID
`string`|`$display_type`|What type to display\. Can be 'single' to only show one verification option or 'all' to show all of them
`bool`|`$reset`|Whether to reset the internal tracking counter

