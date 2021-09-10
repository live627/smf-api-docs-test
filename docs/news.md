---
layout: default
group: func
navtitle: News.php
title: ./Sources/News.php
count: 11
---
* auto-gen TOC:
{:toc}
### ShowXmlFeed

```php
function ShowXmlFeed()
```
Outputs xml data representing recent information or a profile.

Can be passed subactions which decide what is output:
 'recent' for recent posts,
 'news' for news topics,
 'members' for recently registered members,
 'profile' for a member's profile.
 'posts' for a member's posts.
 'personal_messages' for a member's personal messages.

When displaying a member's profile or posts, the u parameter identifies which member. Defaults
to the current user's id.
To display a member's personal messages, the u parameter must match the id of the current user.

Outputs can be in RSS 0.92, RSS 2, Atom, RDF, or our own custom XML format. Default is RSS 2.

Accessed via ?action=.xml.

Does not use any templates, sub templates, or template layers.

Uses Stats, Profile, Post, and PersonalMessage language files.

### buildXmlFeed

```php
function buildXmlFeed($xml_format, $xml_data, $feed_meta, $subaction)
```
### fix_possible_url

```php
function fix_possible_url($val)
```
Called from dumpTags to convert data to xml
Finds urls for local site and sanitizes them



Type|Parameter|Description
---|---|---
`string`|`$val`|A string containing a possible URL

### cdata_parse

```php
function cdata_parse($data, $ns = '', $force = false)
```
Ensures supplied data is properly encapsulated in cdata xml tags
Called from getXmlProfile in News.php



Type|Parameter|Description
---|---|---
`string`|`$data`|XML data
`string`|`$ns`|A namespace prefix for the XML data elements (used by mods, maybe)
`bool`|`$force`|If true, enclose the XML data in cdata tags no matter what (used by mods, maybe)

### dumpTags

```php
function dumpTags($data, $i, $xml_format = '', $forceCdataKeys = array(), $nsKeys = array())
```
Formats data retrieved in other functions into xml format.

Additionally formats data based on the specific format passed.
This function is recursively called to handle sub arrays of data.

Type|Parameter|Description
---|---|---
`array`|`$data`|The array to output as xml data
`int`|`$i`|The amount of indentation to use.
`string`|`$xml_format`|The format to use ('atom', 'rss', 'rss2' or empty for plain XML)
`array`|`$forceCdataKeys`|A list of keys on which to force cdata wrapping (used by mods, maybe)
`array`|`$nsKeys`|Key-value pairs of namespace prefixes to pass to cdata_parse() (used by mods, maybe)

### getXmlMembers

```php
function getXmlMembers($xml_format, $ascending = false)
```
Retrieve the list of members from database.

The array will be generated to match the format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The format to use. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'
`bool`|`$ascending`|If true, get the earliest members first. Default false.

### getXmlNews

```php
function getXmlNews($xml_format, $ascending = false)
```
Get the latest topics information from a specific board,
to display later.

The returned array will be generated to match the xml_format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'.
`bool`|`$ascending`|If true, get the oldest topics first. Default false.

### getXmlRecent

```php
function getXmlRecent($xml_format)
```
Get the recent topics to display.

The returned array will be generated to match the xml_format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'

### getXmlProfile

```php
function getXmlProfile($xml_format)
```
Get the profile information for member into an array,
which will be generated to match the xml_format.



Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'

### getXmlPosts

```php
function getXmlPosts($xml_format, $ascending = false)
```
Get a user's posts.

The returned array will be generated to match the xml_format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'
`bool`|`$ascending`|If true, get the oldest posts first. Default false.

### getXmlPMs

```php
function getXmlPMs($xml_format, $ascending = false)
```
Get a user's personal messages.

Only the user can do this, and no one else -- not even the admin!

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'
`bool`|`$ascending`|If true, get the oldest PMs first. Default false.

