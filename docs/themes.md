---
layout: default
group: func
navtitle: Themes.php
title: ./Sources/Themes.php
count: 17
---
* auto-gen TOC:
{:toc}
### ThemesMain

```php
function ThemesMain(): void
```
Subaction handler - manages the action and delegates control to the proper
sub-action.

It loads both the Themes and Settings language files.
Checks the session by GET or POST to verify the sent data.
Requires the user not be a guest. (@todo what?)
Accessed via ?action=admin;area=theme.

### ThemeAdmin

```php
function ThemeAdmin(): void
```
This function allows administration of themes and their settings,
as well as global theme settings.

- sets the settings theme_allow, theme_guests, and knownThemes.
 - requires the admin_forum permission.
 - accessed with ?action=admin;area=theme;sa=admin.

Uses Themes template
Uses Admin language file

### ThemeList

```php
function ThemeList(): void
```
This function lists the available themes and provides an interface to reset
the paths of all the installed themes.



### SetThemeOptions

```php
function SetThemeOptions(): void
```
Administrative global settings.



### SetThemeSettings

```php
function SetThemeSettings(): void
```
Administrative global settings.

- saves and requests global theme settings. ($settings)
- loads the Admin language file.
- calls ThemeAdmin() if no theme is specified. (the theme center.)
- requires admin_forum permission.
- accessed with ?action=admin;area=theme;sa=list&th=xx.

### RemoveTheme

```php
function RemoveTheme(): void
```
Remove a theme from the database.

- removes an installed theme.
- requires an administrator.
- accessed with ?action=admin;area=theme;sa=remove.

### EnableTheme

```php
function EnableTheme(): void
```
Handles enabling/disabling a theme from the admin center



### canPickTheme

```php
function canPickTheme(int $id_member, int $id_theme): bool
```
Determines if a user can change their theme.



Type|Parameter|Description
---|---|---
`int`|`$id_member`|
`int`|`$id_theme`|

### PickTheme

```php
function PickTheme(): void
```
Choose a theme from a list.

allows a user to pick a new theme with an interface.
- uses the Themes template. (pick sub template.)
- accessed with ?action=theme;sa=pick.

### ThemeInstall

```php
function ThemeInstall(): void
```
Installs new themes, calls the respective function according to the install type.

- puts themes in $boardurl/Themes.
- assumes the gzip has a root directory in it. (ie default.)
Requires admin_forum.
Accessed with ?action=admin;area=theme;sa=install.

### InstallFile

```php
function InstallFile(): array
```
Installs a theme from a theme package.

Stores the theme files on a temp dir, on success it renames the dir to the new theme's name. Ends execution with fatal_lang_error() on any error.

### InstallCopy

```php
function InstallCopy(): array
```
Makes a copy from the default theme, assigns a name for it and installs it.

Creates a new .xml file containing all the theme's info.

### InstallDir

```php
function InstallDir(): array
```
Install a theme from a specific dir

Assumes the dir is located on the main Themes dir. Ends execution with fatal_lang_error() on any error.

### WrapAction

```php
function WrapAction(): void
```
Possibly the simplest and best example of how to use the template system.

- allows the theme to take care of actions.
- happens if $settings['catch_action'] is set and action isn't found
 in the action array.
- can use a template, layers, sub_template, filename, and/or function.

### SetJavaScript

```php
function SetJavaScript(): void
```
Set an option via javascript.

- sets a theme option without outputting anything.
- can be used with javascript, via a dummy image... (which doesn't require
the page to reload.)
- requires someone who is logged in.
- accessed via ?action=jsoption;var=variable;val=value;session_var=sess_id.
- does not log access to the Who's Online log. (in index.php..)

### EditTheme

```php
function EditTheme(): void
```
Shows an interface for editing the templates.

- uses the Themes template and edit_template/edit_style sub template.
- accessed via ?action=admin;area=theme;sa=edit

### CopyTemplate

```php
function CopyTemplate(): void
```
Makes a copy of a template file in a new location



