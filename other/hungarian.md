---
title: Hungarian Notation
group: other
groupname: other
---
* auto-gen TOC:
{:toc}
Hungarian notation is often hastily dismissed without a thorough understanding of its utility. It has been relegated to the same category as the deprecated 'goto' statement, with individuals mindlessly adhering to the mantra of 'don't use goto... don't use goto...'. However, the reality is that Hungarian notation is merely a tool in the developer's arsenal. Like any tool, it has its appropriate applications as well as scenarios where its usage may be less advisable or even detrimental. Drawing parallels, it's akin to someone having had a negative experience attempting to saw wood with a hammer and subsequently advocating against the use of hammers altogether, favoring saws exclusively. Such sweeping generalizations invariably oversimplify complex considerations.

## Naming Convention
Hungarian Notation is a language agnostic naming convention that prefixes variables with the variable's type. This allows the reader to determine the type and use of a variable by such an identifier.

Since JavaScript is dynamically typed this rule makes it easier to see the expected type of a variable.

| Sample | Type |
|-|-|
| `sId` | string |
| `oDomRef` | object |
| `$DomRef` | jQuery object |
| `iCount` | int (`Number`) |
| `aEntries` | array |
| `bEnabled` | boolean |
| `rPattern` | RegExp |
| `funcFunction` | function |

```javascript
var aData = [1, 2, 3];
var bFound = false;
var funcCallback = function() { };
var iCurrentPage = 1;
var nNewRow = document.createElement("tr");
var oSettings = {
    type: "GET",
    url: "test.json",
    dataType: "jsonp"
};
var sLabel = "First Name";
```
