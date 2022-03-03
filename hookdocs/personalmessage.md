---
layout: default
group: hooks
title: Personalmessage
count: 5
---
{:toc}
## PersonalMessage.php
### integrate_conversation_buttons

```php
call_integration_hook('integrate_conversation_buttons')
```


Called from
: [`MessageFolder()` in `./Sources/PersonalMessage.php`](../docs/personalmessage.html#messagefolder)

Notes
: Since 2.1

### integrate_prepare_pm_context

```php
call_integration_hook('integrate_prepare_pm_context', array(&$output, &$message, $counter))
```

Type|Parameter|Description
---|---|---
`array`|`&$output`|desc
`array`|`&$message`|desc
`array`|`$counter`|desc

Called from
: [`prepareMessageContext()` in `./Sources/PersonalMessage.php`](../docs/personalmessage.html#preparemessagecontext)

Notes
: Since 2.1

### integrate_search_pm_context

```php
call_integration_hook('integrate_search_pm_context')
```


Called from
: [`MessageSearch2()` in `./Sources/PersonalMessage.php`](../docs/personalmessage.html#messagesearch2)

Notes
: Since 2.1

### integrate_pm_post

```php
call_integration_hook('integrate_pm_post')
```


Called from
: [`MessagePost()` in `./Sources/PersonalMessage.php`](../docs/personalmessage.html#messagepost)

Notes
: Since 2.1

### integrate_pm_error

```php
call_integration_hook('integrate_pm_error')
```


Called from
: [`messagePostError()` in `./Sources/PersonalMessage.php`](../docs/personalmessage.html#messageposterror)

Notes
: Since 2.1

