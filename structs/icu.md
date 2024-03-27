---
title: Message Syntax
group: structs
groupname: structs
---
* auto-gen TOC:
{:toc}

If you are translating text you'll need a way for your translators to express the subtleties of spelling, grammar, and conjugation inherent in each language. We use the [ICU Message syntax](https://unicode-org.github.io/icu/userguide/format_parse/messages) which is also used in Java and PHP.

Basic Principles[​](#basic-principles "Direct link to Basic Principles")
------------------------------------------------------------------------

The simplest transform for the message is a literal string.

    Hello everyone

All other transforms are done using replacements called "arguments". They are enclosed in curly braces (`{` and `}`) and refer to a value in the input data.

Simple Argument[​](#simple-argument "Direct link to Simple Argument")
---------------------------------------------------------------------

You can use a `{key}` argument for placing a value into the message. The key is looked up in the input data, and the string is interpolated with its value.

```php
// Language file
$txt['sample'] = 'Hello, {who}.';

// Source code
\SMF\Lang::getTxt('sample', ['who' => 'world']);
```

Output
 : Hello, world.

## Formatted Argument

Values can also be formatted based on their type. You use a `{key, type, format}` argument to do that.

The elements of the argument are:

*   `key` is where in the input data to find the data
*   `type` is optional, and is how to interpret the value (see below)
*   `format` is optional, and is a further refinement on how to display that type of data

ICU Message

I have {numCats, number} cats.

Values as JSON

Result

### `number` Type[​](#number-type "Direct link to number-type")

This type is used to format numbers in a way that is sensitive to the locale. It understands the following values for the optional `format` element of the argument:

ICU Message

I have {numCats, number} cats.

Values as JSON

Result

ICU Message

Almost {pctBlack, number, ::percent} of them are black.

Values as JSON

Result

Internally it uses the Intl.NumberFormat API. You can define custom values for the `format` element, which are passed to the Intl.NumberFormat constructor.

Sometimes embedding how the number will be formatted provides great context to translators. We also support ICU Number Skeletons using the same syntax:

ICU Message

The price of this bagel is {num, number, ::sign-always compact-short currency/GBP}

Values as JSON

Result

You can read more about this [here](https://unicode-org.github.io/icu/userguide/format_parse/numbers/skeletons.html).

For fine control over decimal precision, you can use the Fraction Precision `#` and `0` symbols, which specify the number of decimal places to display:

ICU Message

The duration is {num, number, ::.##} seconds

Values as JSON

Result

Note that the `#` symbol doesn't render trailing zeroes, as seen in this example:

ICU Message

The duration is {num, number, ::.##} seconds

Values as JSON

Result

To render trailing zeroes, use the `0` symbol:

ICU Message

The very precise number is {num, number, ::.00}

Values as JSON

Result

For more details, see [Fraction Precision](https://unicode-org.github.io/icu/userguide/format_parse/numbers/skeletons.html#fraction-precision).

### `date` Type[​](#date-type "Direct link to date-type")

This type is used to format dates in a way that is sensitive to the locale. It understands the following values for the optional format element of the argument:

*   `short` is used to format dates in the shortest possible way
*   `medium` is used to format dates with short textual representation of the month
*   `long` is used to format dates with long textual representation of the month
*   `full` is used to format dates with the most detail

ICU Message

Sale begins {start, date, medium}

Values as JSON

Result

Internally it uses the `Intl.DateTimeFormat` API. You can define custom values for the format element, which are passed to the `Intl.DateTimeFormat` constructor.

### `time` Type[​](#time-type "Direct link to time-type")

This type is used to format times in a way that is sensitive to the locale. It understands the following values for the optional format element of the argument:

*   `short` is used to format times with hours and minutes
*   `medium` is used to format times with hours, minutes, and seconds
*   `long` is used to format times with hours, minutes, seconds, and timezone
*   `full` is the same as long

ICU Message

Coupon expires at {expire, time, short}

Values as JSON

Result

Internally it uses the `Intl.DateTimeFormat` API. You can define custom values for the format element, which are passed to the `Intl.DateTimeFormat` constructor.

### Supported DateTime Skeleton[​](#supported-datetime-skeleton "Direct link to Supported DateTime Skeleton")

Similar to `number` type, we also support ICU DateTime skeleton. ICU provides a [wide array of pattern](https://unicode-org.github.io/icu/userguide/format_parse/datetime/#date-field-symbol-table) to customize date time format. However, not all of them are available via ECMA402's Intl API. Therefore, we only support the following patterns

Symbol

Meaning

Notes

G

Era designator

y

year

M

month in year

L

stand-alone month in year

d

day in month

E

day of week

e

local day of week

`e..eee` is not supported

c

stand-alone local day of week

`c..ccc` is not supported

a

AM/PM marker

h

Hour \[1-12\]

H

Hour \[0-23\]

K

Hour \[0-11\]

k

Hour \[1-24\]

m

Minute

s

Second

z

Time Zone

### `{select}` Format[​](#select-format "Direct link to select-format")

The `{key, select, matches}` is used to choose output by matching a value to one of many choices. (It is similar to the `switch` statement available in some programming languages.) The key is looked up in the input data. The corresponding value is matched to one of matches and the corresponding output is returned. The `key` argument must follow [Unicode Pattern\_Syntax](https://www.unicode.org/reports/tr31/tr31-9.html#Pattern_Syntax). The `matches` is a space-separated list of `matches`.

The format of a match is match `{output}`. (A match is similar to the case statement of the switch found in some programming languages.) The `match` is a literal value. If it is the same as the value for `key` then the corresponding `output` will be used.

output is itself a message, so it can be a literal string or also have more arguments nested inside of it.

The `other` match is special and is used if nothing else matches. (This is similar to the default case of the switch found in some programming languages.)

danger

`other` is required as per `icu4j` implementation. We will throw an error if `select` is used without `other`.

ICU Message

{gender, select,
    male {He will respond shortly.}
    female {She will respond shortly.}
    other {They will respond shortly.}
}

Values as JSON

Result

Here's an example of nested arguments.

ICU Message

{isTaxed, select,
    yes {An additional {tax, number, percent} tax will be collected.}
    other {No taxes apply.}
}

Values as JSON

Result

### `{plural}` Format[​](#plural-format "Direct link to plural-format")

The `{key, plural, matches}` is used to choose output based on the pluralization rules of the current locale. It is very similar to the `{select}` format above except that the value is expected to be a number and is mapped to a plural category.

The match is a literal value and is matched to one of these plural categories. Not all languages use all plural categories.

*   `zero`: This category is used for languages that have grammar specialized specifically for zero number of items. (Examples are Arabic and Latvian.)
*   `one`: This category is used for languages that have grammar specialized specifically for one item. Many languages, but not all, use this plural category. (Many popular Asian languages, such as Chinese and Japanese, do not use this category.)
*   `two`: This category is used for languages that have grammar specialized specifically for two items. (Examples are Arabic and Welsh.)
*   `few`: This category is used for languages that have grammar specialized specifically for a small number of items. For some languages this is used for 2-4 items, for some 3-10 items, and other languages have even more complex rules.
*   `many`: This category is used for languages that have grammar specialized specifically for a larger number of items. (Examples are Arabic, Polish, and Russian.)
*   `other`: This category is used if the value doesn't match one of the other plural categories. Note that this is used for "plural" for languages (such as English) that have a simple "singular" versus "plural" dichotomy.
*   `=value`: This is used to match a specific value regardless of the plural categories of the current locale.

danger

`other` is required as per `icu4j` implementation. We will throw an error if `plural` is used without `other`.

ICU Message

{itemCount, plural,
    one {Cart: {itemCount, number} item}
    other {Cart: {itemCount, number} items}
}

Values as JSON

Result

ICU Message

{itemCount, plural,
    =0 {You have no items.}
    one {You have {itemCount, number} item.}
    other {You have {itemCount, number} items.}
}

Values as JSON

Result

In the `output` of the match, you can use the `#` special token as a placeholder for the numeric value and it'll be formatted as if it were `{key, number}`. This is the style we prefer to use.

ICU Message

{itemCount, plural,
    =0 {You have no items.}
    one {You have # item.}
    other {You have # items.}
}

Values as JSON

Result

### `{selectordinal}` Format[​](#selectordinal-format "Direct link to selectordinal-format")

The `{key, selectordinal, matches}` is used to choose output based on the ordinal pluralization rules (1st, 2nd, 3rd, etc.) of the current locale. It is very similar to the {plural} format above except that the value is mapped to an ordinal plural category.

The match is a literal value and is matched to one of these plural categories. Not all languages use all plural categories.

*   `zero`: This category is used for languages that have grammar specialized specifically for zero number of items. (Examples are Arabic and Latvian.)
*   `one`: This category is used for languages that have grammar specialized specifically for one item. Many languages, but not all, use this plural category. (Many popular Asian languages, such as Chinese and Japanese, do not use this category.)
*   `two`: This category is used for languages that have grammar specialized specifically for two items. (Examples are Arabic and Welsh.)
*   `few`: This category is used for languages that have grammar specialized specifically for a small number of items. For some languages this is used for 2-4 items, for some 3-10 items, and other languages have even more complex rules.
*   `many`: This category is used for languages that have grammar specialized specifically for a larger number of items. (Examples are Arabic, Polish, and Russian.)
*   `other`: This category is used if the value doesn't match one of the other plural categories. Note that this is used for "plural" for languages (such as English) that have a simple "singular" versus "plural" dichotomy.
*   `=value`: This is used to match a specific value regardless of the plural categories of the current locale.

danger

`other` is required as per `icu4j` implementation. We will throw an error if `selectordinal` is used without `other`.

In the `output` of the match, the `#` special token can be used as a placeholder for the numeric value and will be formatted as if it were `{key, number}`.

ICU Message

It's my cat's {year, selectordinal,
    one {#st}
    two {#nd}
    few {#rd}
    other {#th}
} birthday!

Values as JSON

Result

Rich Text Formatting[​](#rich-text-formatting "Direct link to Rich Text Formatting")
------------------------------------------------------------------------------------

We also support embedded rich text formatting in our message using tags. This allows developers to embed as much text as possible so sentences don't have to be broken up into chunks **NOTE: This is not XML/HTML tag**

ICU Message

Our price is <boldThis>{price, number, ::currency/USD precision-integer}</boldThis>
with <link>{pct, number, ::percent} discount</link>

Values as JSON

Result

Custom Behavior

It is expected that the system using embedded rich text formatting will have methods to handle these placeholders external to this library. The tags will be part of the generated output and can either be **post-processed** by your own tooling or use the [defaultRichTextElements](/docs/intl/#defaultRichTextElements) configuration.

Quoting / Escaping[​](#quoting--escaping "Direct link to Quoting / Escaping")
-----------------------------------------------------------------------------

The ASCII apostrophe `'` (U+0027) can be used to escape syntax characters in the text portion of the message, which mimics the [behavior of ICU's quoting/escaping](https://unicode-org.github.io/icu/userguide/format_parse/messages/#quotingescaping).

ICU Message

This is not an interpolation: '{word}

Values as JSON

Result

ICU Message

These are not interpolations: '{word1} {word2}'

Values as JSON

Result

ICU Message

'<notATag>

Values as JSON

Result

ICU Message

'<notATag>hello</notATag>'

Values as JSON

Result

Two consecutive ASCII apostrophes represents one ASCII apostrophe, similar to `%%` in `printf` represents one `%`. However, we recommend using curly apostrophe `’` (U+2019) for human-readable strings and only use ASCII apostrophe `'` (U+0027) in ICU message syntax.

ICU Message

This '{isn''t}' obvious.

Values as JSON

Result
