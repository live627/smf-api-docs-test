---
title: Naming Conventions
group: other
groupname: other
---
* auto-gen TOC:
{:toc}
Several naming conventions for variables exist which you should be aware of. Beginners to programming and scripting often overlook these, but they help maintain order in an often chaotic field.

Here are several commonly used conventions:

🐫 **Camel Case**: Begins with a lowercase letter, with subsequent words capitalized. Examples: newVariable, iLikeCamelCase. Suitable for assigning string, number, boolean, object, array, list, etc.

👵🏽 **Pascal Case**: Similar to Camel Case but starts with a capital letter. Examples: NewVariable, ILikeItToo. Primarily employed for declaring classes and their types (Object Constructor Function, Interface...).

🐍 **Snake Case**: Utilizes lowercase letters with underscore (`_`) separation, like `this_one`. Ideal for object keys and database fields. Also useful for declaring lengthy variables, such as really_really_loooong_variable.

🍖 **Kebab Case**: Concatenates lowercase letters with hyphens, as in `just-like-this-example`. Suitable for routes (URLs), among other uses.

😠 **Screaming Case**: Employs all capital letters to convey emphasis. Useful for hardcoding values, such as `TAX` = 10%, using SCREAMING_CASE.

⁉️ **Hungarian Notation**: Prefixes names with a lowercase indicator to convey intention. Examples include `sName and `nAge`. While JavaScript lacks strict typing (e.g., string, number...), Hungarian notation offers hints about a variable's type (s for string, n for number...).

**_Underscore before a variable**: Commonly denotes a `_privateVariable` inaccessible outside of a class.

Happy Coding! 👋
