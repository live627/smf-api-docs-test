---
layout: default
group: hooks
title: Modifying application flow
---
* auto-gen TOC:
{:toc}
### integrate_buffer

Type|Parameter|Description
---|---|---
`string`|`$buffer`|Callback to [`ob_start()`](https://www.php.net/manual/en/function.ob-start.php)

Called from
: obExit()

Notes
: It MUST return a `string`, exactly like a normal buffer callback would, because it really is one!

### integrate_exit

Type|Parameter|Description
---|---|---
`bool`|`$do_footer`|whether the footer should be output or not

Called from
: obExit()

Notes
: This is among the very last calls before the program is done running.
: Run any last minute cleanup, a final shutdown on external apps, close connections, and free any resources. Can also be used with portals or other output handling functions.

### integrate_fix_url

Type|Parameter|Description
---|---|---
`string`|`&$val`|A possible URL

Called from
: fix_possible_url()

Notes
: This won't be called if the possible URL starts with `$scripturl`.

### integrate_redirect

Type|Parameter|Description
---|---|---
`string`|`&$setLocation`|The URL to redirect them to
`bool`|`&$refresh`|Whether to send a Refresh header instead of a Location header
`bool`|`&$permanent`|Whether to send a 301 Moved Permanently instead of a 302 Moved Temporarily

Called from
: redirectexit()
