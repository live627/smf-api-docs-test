---
layout: default
group: func
navtitle: Reports.php
title: ./Sources/Reports.php
count: 11
---
* auto-gen TOC:
{:toc}
### ReportsMain

```php
function ReportsMain(): void
```
Handling function for generating reports.

Requires the admin_forum permission.
Loads the Reports template and language files.
Decides which type of report to generate, if this isn't passed
through the querystring it will set the report_type sub-template to
force the user to choose which type.
When generating a report chooses which sub_template to use.
Depends on the cal_enabled setting, and many of the other cal_
settings.
Will call the relevant report generation function.
If generating report will call finishTables before returning.
Accessed through ?action=admin;area=reports.

### BoardReport

```php
function BoardReport(): void
```
Standard report about what settings the boards have.

functions ending with "Report" are responsible for generating data
for reporting.
they are all called from ReportsMain.
never access the context directly, but use the data handling
functions to do so.

### BoardPermissionsReport

```php
function BoardPermissionsReport(): void
```
Generate a report on the current permissions by board and membergroup.

functions ending with "Report" are responsible for generating data
for reporting.
they are all called from ReportsMain.
never access the context directly, but use the data handling
functions to do so.

### MemberGroupsReport

```php
function MemberGroupsReport(): void
```
Show what the membergroups are made of.

functions ending with "Report" are responsible for generating data
for reporting.
they are all called from ReportsMain.
never access the context directly, but use the data handling
functions to do so.

### GroupPermissionsReport

```php
function GroupPermissionsReport(): void
```
Show the large variety of group permissions assigned to each membergroup.

functions ending with "Report" are responsible for generating data
for reporting.
they are all called from ReportsMain.
never access the context directly, but use the data handling
functions to do so.

### StaffReport

```php
function StaffReport(): void
```
Report for showing all the forum staff members - quite a feat!
functions ending with "Report" are responsible for generating data
for reporting.

they are all called from ReportsMain.
never access the context directly, but use the data handling
functions to do so.

### newTable

```php
function newTable(string $title = '', string $default_value = '', string $shading = 'all', string $width_normal = 'auto', string $align_normal = 'center', string $width_shaded = 'auto', string $align_shaded = 'auto'): void
```
This function creates a new table of data, most functions will only use it once.

The core of this file, it creates a new, but empty, table of data in
context, ready for filling using addData().
Fills the context variable current_table with the ID of the table created.
Keeps track of the current table count using context variable table_count.

Type|Parameter|Description
---|---|---
`string`|`$title`|Title to be displayed with this data table.
`string`|`$default_value`|Value to be displayed if a key is missing from a row.
`string`|`$shading`|Should the left, top or both (all) parts of the table beshaded?
`string`|`$width_normal`|The width of an unshaded column (auto means not defined).
`string`|`$align_normal`|The alignment of data in an unshaded column.
`string`|`$width_shaded`|The width of a shaded column (auto means not defined).
`string`|`$align_shaded`|The alignment of data in a shaded column.

### addData

```php
function addData(array $inc_data, ?string $custom_table = null): void|false
```
Adds an array of data into an existing table.

if there are no existing tables, will create one with default
attributes.
if custom_table isn't specified, it will use the last table created,
if it is specified and doesn't exist the function will return false.
if a set of keys have been specified, the function will check each
required key is present in the incoming data. If this data is missing
the current tables default value will be used.
if any key in the incoming data begins with '#sep#', the function
will add a separator across the table at this point.
once the incoming data has been sanitized, it is added to the table.

Type|Parameter|Description
---|---|---
`array`|`$inc_data`|The data to include
`null&#124;string`|`$custom_table`|= null The ID of a custom table to put the data in

### addSeparator

```php
function addSeparator(string $title = '', ?string $custom_table = null): void|bool
```
Add a separator row, only really used when adding data by rows.



Type|Parameter|Description
---|---|---
`string`|`$title`|The title of the separator
`null&#124;string`|`$custom_table`|The ID of the custom table

### finishTables

```php
function finishTables(): void
```
This does the necessary count of table data before displaying them.

is (unfortunately) required to create some useful variables for templates.
foreach data table created, it will count the number of rows and
columns in the table.
will also create a max_width variable for the table, to give an
estimate width for the whole table * * if it can.

### setKeys

```php
function setKeys(string $method = 'rows', array $keys = array(), bool $reverse = false): void
```
Set the keys in use by the tables - these ensure entries MUST exist if the data isn't sent.

sets the current set of "keys" expected in each data array passed to
addData. It also sets the way we are adding data to the data table.
method specifies whether the data passed to addData represents a new
column, or a new row.
keys is an array whose keys are the keys for data being passed to
addData().
if reverse is set to true, then the values of the variable "keys"
are used as opposed to the keys(!

Type|Parameter|Description
---|---|---
`string`|`$method`|The method. Can be 'rows' or 'columns'
`array`|`$keys`|The keys
`bool`|`$reverse`|Whether we want to use the values as the keys

