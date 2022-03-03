---
layout: default
group: hooks
title: Messageindex
count: 4
---
{:toc}
## MessageIndex.php
### integrate_pre_messageindex

```php
call_integration_hook('integrate_pre_messageindex', array(&$sort_methods, &$sort_methods_table))
```

Type|Parameter|Description
---|---|---
`array`|`&$sort_methods`|desc
`array`|`&$sort_methods_table`|desc

Called from
: [`MessageIndex()` in `./Sources/MessageIndex.php`](../docs/messageindex.html#messageindex)

Notes
: Since 2.1

### integrate_message_index

```php
call_integration_hook('integrate_message_index', array(&$message_index_selects, &$message_index_tables, &$message_index_parameters, &$message_index_wheres, &$topic_ids, &$message_index_topic_wheres))
```

Type|Parameter|Description
---|---|---
`array`|`&$message_index_selects`|desc
`array`|`&$message_index_tables`|desc
`array`|`&$message_index_parameters`|desc
`array`|`&$message_index_wheres`|desc
`array`|`&$topic_ids`|desc
`array`|`&$message_index_topic_wheres`|desc

Called from
: [`MessageIndex()` in `./Sources/MessageIndex.php`](../docs/messageindex.html#messageindex)

Notes
: Since 2.1

### integrate_quick_mod_actions

```php
call_integration_hook('integrate_quick_mod_actions')
```


Called from
: [`MessageIndex()` in `./Sources/MessageIndex.php`](../docs/messageindex.html#messageindex)

Notes
: Since 2.1

### integrate_messageindex_buttons

```php
call_integration_hook('integrate_messageindex_buttons', array(&$context['normal_buttons']))
```

Type|Parameter|Description
---|---|---
`array`|`&$normal_buttons`|desc

Called from
: [`MessageIndex()` in `./Sources/MessageIndex.php`](../docs/messageindex.html#messageindex)

Notes
: Since 2.1

