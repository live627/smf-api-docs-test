---
layout: default
group: func
navtitle: Subs-Timezones.php
title: ./Sources/Subs-Timezones.php
count: 4
---
* auto-gen TOC:
{:toc}
### get_tzid_metazones

```php
function get_tzid_metazones(string $when = 'now'): array
```
Returns an array that instructs SMF how to map specific time zones
(e.g. "America/Denver") onto the user-friendly "meta-zone" labels that
most people think of as time zones (e.g. "Mountain Time").



Type|Parameter|Description
---|---|---
`string`|`$when`|The date/time used to determine fallback values.
||May be a Unix timestamp or any string that strtotime() can understand.
||Defaults to 'now'.

Integration hooks
: integrate_metazones

### get_sorted_tzids_for_country

```php
function get_sorted_tzids_for_country(string $country_code, string $when = 'now'): array
```
Returns an array of all the time zones in a country, ranked according
to population and/or political significance.



Type|Parameter|Description
---|---|---
`string`|`$country_code`|The two-character ISO-3166 code for a country.
`string`|`$when`|The date/time used to determine fallback values.
||May be a Unix timestamp or any string that strtotime() can understand.
||Defaults to 'now'.

Integration hooks
: integrate_country_timezones

### get_tzid_fallbacks

```php
function get_tzid_fallbacks(array $tzids, string $when = 'now'): array
```
Checks a list of time zone identifiers to make sure they are all defined in
the installed version of the time zone database, and returns an array of
key-value substitution pairs.

For defined time zone identifiers, the substitution value will be identical
to the original value. For undefined ones, the substitute will be a time zone
identifier that was equivalent to the missing one at the specified time, or
an empty string if there was no equivalent at that time.

Note: These fallbacks do not need to include every new time zone ever. They
only need to cover any that are used in $tzid_metazones.

To find the date & time when a new time zone comes into effect, check
the TZDB changelog at https://data.iana.org/time-zones/tzdb/NEWS

Type|Parameter|Description
---|---|---
`array`|`$tzids`|The time zone identifiers to check.
`string`|`$when`|The date/time used to determine substitute values.
||May be a Unix timestamp or any string that strtotime() can understand.
||Defaults to 'now'.

Integration hooks
: integrate_timezone_fallbacks

### validate_iso_country_codes

```php
function validate_iso_country_codes(array|string $country_codes, bool $as_csv = false): array|string
```
Validates a set of two-character ISO 3166-1 country codes.



Type|Parameter|Description
---|---|---
`array`&#124;`string`|`$country_codes`|Array or CSV string of country codes.
`bool`|`$as_csv`|If true, return CSV string instead of array.

