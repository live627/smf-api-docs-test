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
function ShowXmlFeed(): void
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

Integration hooks
: integrate_xmlfeeds

### buildXmlFeed

```php
function buildXmlFeed($xml_format, $xml_data, $feed_meta, $subaction)
```
Integration hooks
: integrate_xml_data

### fix_possible_url

```php
function fix_possible_url(string $val): string
```
Called from dumpTags to convert data to xml
Finds urls for local site and sanitizes them



Type|Parameter|Description
---|---|---
`string`|`$val`|A string containing a possible URL

Integration hooks
: integrate_fix_url

### cdata_parse

```php
function cdata_parse(string $data, string $ns = '', bool $force = false): string
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
function dumpTags(array $data, int $i, string $xml_format = '', array $forceCdataKeys = array(), array $nsKeys = array()): void
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
function getXmlMembers(string $xml_format, bool $ascending = false): array
```
Retrieve the list of members from database.

The array will be generated to match the format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The format to use. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'
`bool`|`$ascending`|If true, get the earliest members first. Default false.

### getXmlNews

```php
function getXmlNews(string $xml_format, bool $ascending = false): array
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
function getXmlRecent(string $xml_format): array
```
Get the recent topics to display.

The returned array will be generated to match the xml_format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'

### getXmlProfile

```php
function getXmlProfile(string $xml_format): array
```
Get the profile information for member into an array,
which will be generated to match the xml_format.



Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'

### getXmlPosts

```php
function getXmlPosts(string $xml_format, bool $ascending = false): array
```
Get a user's posts.

The returned array will be generated to match the xml_format.

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'
`bool`|`$ascending`|If true, get the oldest posts first. Default false.

### getXmlPMs

```php
function getXmlPMs(string $xml_format, bool $ascending = false): array
```
Get a user's personal messages.

Only the user can do this, and no one else -- not even the admin!

Type|Parameter|Description
---|---|---
`string`|`$xml_format`|The XML format. Can be 'atom', 'rdf', 'rss', 'rss2' or 'smf'
`bool`|`$ascending`|If true, get the oldest PMs first. Default false.

