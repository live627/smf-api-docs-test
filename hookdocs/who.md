---
layout: default
group: hooks
title: Who.php
count: 4
---
* auto-gen TOC:
{:toc}
### who_allowed

```php
call_integration_hook('who_allowed', array(&$allowedActions))
```

Type|Parameter|Description
---|---|---
`array`|`&$allowedActions`|desc

Called from
: [`determineActions()` in `./Sources/Who.php`](../docs/who.html#determineactions)

Notes
: Since 2.1

### integrate_whos_online

```php
call_integration_hook('integrate_whos_online', array($actions))
```

Type|Parameter|Description
---|---|---
`array`|`$actions`|desc

Called from
: [`determineActions()` in `./Sources/Who.php`](../docs/who.html#determineactions)

Notes
: Since 2.1

### whos_online_after

```php
call_integration_hook('whos_online_after', array(&$urls, &$data))
```

Type|Parameter|Description
---|---|---
`array`|`&$urls`|desc
`array`|`&$data`|desc

Called from
: [`determineActions()` in `./Sources/Who.php`](../docs/who.html#determineactions)

Notes
: Since 2.1

### integrate_credits

```php
call_integration_hook('integrate_credits')
```


Called from
: [`Credits()` in `./Sources/Who.php`](../docs/who.html#credits)

Notes
: Since 2.1

