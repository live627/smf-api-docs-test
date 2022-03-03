---
layout: default
group: hooks
title: Search
count: 12
---
{:toc}
## Search.php
### integrate_search

```php
call_integration_hook('integrate_search')
```


Called from
: [`PlushSearch1()` in `./Sources/Search.php`](../docs/search.html#plushsearch1)

Notes
: Since 2.1

### integrate_search_weights

```php
call_integration_hook('integrate_search_weights', array(&$weight_factors))
```

Type|Parameter|Description
---|---|---
`array`|`&$weight_factors`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_search_sort_columns

```php
call_integration_hook('integrate_search_sort_columns', array(&$sort_columns))
```

Type|Parameter|Description
---|---|---
`array`|`&$sort_columns`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_search_params

```php
call_integration_hook('integrate_search_params', array(&$search_params))
```

Type|Parameter|Description
---|---|---
`array`|`&$search_params`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_search_blacklisted_words

```php
call_integration_hook('integrate_search_blacklisted_words', array(&$blacklisted_words))
```

Type|Parameter|Description
---|---|---
`array`|`&$blacklisted_words`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_search_errors

```php
call_integration_hook('integrate_search_errors')
```


Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_subject_only_search_query

```php
call_integration_hook('integrate_subject_only_search_query', array(&$subject_query, &$subject_query_params))
```

Type|Parameter|Description
---|---|---
`array`|`&$subject_query`|desc
`array`|`&$subject_query_params`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_subject_search_query

```php
call_integration_hook('integrate_subject_search_query', array(&$subject_query))
```

Type|Parameter|Description
---|---|---
`array`|`&$subject_query`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_main_search_query

```php
call_integration_hook('integrate_main_search_query', array(&$main_query))
```

Type|Parameter|Description
---|---|---
`array`|`&$main_query`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_search_message_list

```php
call_integration_hook('integrate_search_message_list', array(&$msg_list, &$posters))
```

Type|Parameter|Description
---|---|---
`array`|`&$msg_list`|desc
`array`|`&$posters`|desc

Called from
: [`PlushSearch2()` in `./Sources/Search.php`](../docs/search.html#plushsearch2)

Notes
: Since 2.1

### integrate_quick_mod_actions_search

```php
call_integration_hook('integrate_quick_mod_actions_search')
```


Called from
: [`prepareSearchContext()` in `./Sources/Search.php`](../docs/search.html#preparesearchcontext)

Notes
: Since 2.1

### integrate_search_message_context

```php
call_integration_hook('integrate_search_message_context', array(&$output, &$message, $counter))
```

Type|Parameter|Description
---|---|---
`array`|`&$output`|desc
`array`|`&$message`|desc
`array`|`$counter`|desc

Called from
: [`prepareSearchContext()` in `./Sources/Search.php`](../docs/search.html#preparesearchcontext)

Notes
: Since 2.1

