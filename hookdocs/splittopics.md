---
layout: default
group: hooks
title: Splittopics
count: 2
---
* auto-gen TOC:
{:toc}

## SplitTopics.php
### integrate_split_topic

```php
call_integration_hook('integrate_split_topic', array($split1, $split2, $new_subject, $id_board))
```

Type|Parameter|Description
---|---|---
`array`|`$split1`|desc
`array`|`$split2`|desc
`array`|`$new_subject`|desc
`array`|`$id_board`|desc

Called from
: [`splitTopic()` in `./Sources/SplitTopics.php`](../docs/splittopics.html#splittopic)

Notes
: Since 2.1

### integrate_merge_topic

```php
call_integration_hook('integrate_merge_topic', array($merged_topic, $updated_topics, $deleted_topics, $deleted_polls))
```

Type|Parameter|Description
---|---|---
`array`|`$merged_topic`|desc
`array`|`$updated_topics`|desc
`array`|`$deleted_topics`|desc
`array`|`$deleted_polls`|desc

Called from
: [`MergeExecute()` in `./Sources/SplitTopics.php`](../docs/splittopics.html#mergeexecute)

Notes
: Since 2.1

