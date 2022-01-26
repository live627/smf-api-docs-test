---
layout: default
group: func
navtitle: SSI.php
title: ./SSI.php
count: 40
---
* auto-gen TOC:
{:toc}
### ssi_shutdown

```php
function ssi_shutdown(): void
```
This shuts down the SSI and shows the footer.



### ssi_version

```php
function ssi_version(string $output_method = 'echo'): void|string
```
Show the SMF version.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|If 'echo', displays the version, otherwise returns it

### ssi_full_version

```php
function ssi_full_version(string $output_method = 'echo'): void|string
```
Show the full SMF version string.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|If 'echo', displays the full version string, otherwise returns it

### ssi_software_year

```php
function ssi_software_year(string $output_method = 'echo'): void|string
```
Show the SMF software year.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|If 'echo', displays the software year, otherwise returns it

### ssi_copyright

```php
function ssi_copyright(string $output_method = 'echo'): void|string
```
Show the forum copyright. Only used in our ssi_examples files.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|If 'echo', displays the forum copyright, otherwise returns it

### ssi_welcome

```php
function ssi_welcome(string $output_method = 'echo'): void|array
```
Display a welcome message, like: Hey, User, you have 0 messages, 0 are new.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', will display everything. Otherwise returns an array of user info.

### ssi_menubar

```php
function ssi_menubar(string $output_method = 'echo'): void|array
```
Display a menu bar, like is displayed at the top of the forum.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', will display the menu, otherwise returns an array of menu data.

### ssi_logout

```php
function ssi_logout(string $redirect_to = '', string $output_method = 'echo'): void|string
```
Show a logout link.



Type|Parameter|Description
---|---|---
`string`|`$redirect_to`|A URL to redirect the user to after they log out.
`string`|`$output_method`|The output method. If 'echo', shows a logout link, otherwise returns the HTML for it.

### ssi_recentPosts

```php
function ssi_recentPosts(int $num_recent = 8, ?array $exclude_boards = null, ?array $include_boards = null, string $output_method = 'echo', bool $limit_body = true): void|array
```
Recent post list:   [board] Subject by Poster    Date



Type|Parameter|Description
---|---|---
`int`|`$num_recent`|How many recent posts to display
`null&#124;array`|`$exclude_boards`|If set, doesn't show posts from the specified boards
`null&#124;array`|`$include_boards`|If set, only includes posts from the specified boards
`string`|`$output_method`|The output method. If 'echo', displays the posts, otherwise returns an array of information about them.
`bool`|`$limit_body`|Whether or not to only show the first 384 characters of each post

### ssi_fetchPosts

```php
function ssi_fetchPosts(array $post_ids = array(), bool $override_permissions = false, string $output_method = 'echo'): void|array
```
Fetches one or more posts by ID.



Type|Parameter|Description
---|---|---
`array`|`$post_ids`|An array containing the IDs of the posts to show
`bool`|`$override_permissions`|Whether to ignore permissions. If true, will show posts even if the user doesn't have permission to see them.
`string`|`$output_method`|The output method. If 'echo', displays the posts, otherwise returns an array of info about them

### ssi_queryPosts

```php
function ssi_queryPosts(string $query_where = '', array $query_where_params = array(), int $query_limit = 10, string $query_order = 'm.id_msg DESC', string $output_method = 'echo', bool $limit_body = false, bool|false $override_permissions = false): void|array
```
This handles actually pulling post info. Called from other functions to eliminate duplication.



Type|Parameter|Description
---|---|---
`string`|`$query_where`|The WHERE clause for the query
`array`|`$query_where_params`|An array of parameters for the WHERE clause
`int`|`$query_limit`|The maximum number of rows to return
`string`|`$query_order`|The ORDER BY clause for the query
`string`|`$output_method`|The output method. If 'echo', displays the posts, otherwise returns an array of info about them.
`bool`|`$limit_body`|If true, will only show the first 384 characters of the post rather than all of it
`bool&#124;false`|`$override_permissions`|Whether or not to ignore permissions. If true, will show all posts regardless of whether the user can actually see them

### ssi_recentTopics

```php
function ssi_recentTopics(int $num_recent = 8, ?array $exclude_boards = null, ?array $include_boards = null, string $output_method = 'echo'): void|array
```
Recent topic list:   [board] Subject by Poster   Date



Type|Parameter|Description
---|---|---
`int`|`$num_recent`|How many recent topics to show
`null&#124;array`|`$exclude_boards`|If set, exclude topics from the specified board(s)
`null&#124;array`|`$include_boards`|If set, only include topics from the specified board(s)
`string`|`$output_method`|The output method. If 'echo', displays a list of topics, otherwise returns an array of info about them

### ssi_topPoster

```php
function ssi_topPoster(int $topNumber = 1, string $output_method = 'echo'): void|array
```
Shows a list of top posters



Type|Parameter|Description
---|---|---
`int`|`$topNumber`|How many top posters to list
`string`|`$output_method`|The output method. If 'echo', will display a list of users, otherwise returns an array of info about them.

### ssi_topBoards

```php
function ssi_topBoards(int $num_top = 10, string $output_method = 'echo'): void|array
```
Shows a list of top boards based on activity



Type|Parameter|Description
---|---|---
`int`|`$num_top`|How many boards to display
`string`|`$output_method`|The output method. If 'echo', displays a list of boards, otherwise returns an array of info about them.

### ssi_topTopics

```php
function ssi_topTopics(string $type = 'replies', int $num_topics = 10, string $output_method = 'echo'): void|array
```
Shows a list of top topics based on views or replies



Type|Parameter|Description
---|---|---
`string`|`$type`|Can be either replies or views
`int`|`$num_topics`|How many topics to display
`string`|`$output_method`|The output method. If 'echo', displays a list of topics, otherwise returns an array of info about them.

### ssi_topTopicsReplies

```php
function ssi_topTopicsReplies(int $num_topics = 10, string $output_method = 'echo'): void|array
```
Top topics based on replies



Type|Parameter|Description
---|---|---
`int`|`$num_topics`|How many topics to show
`string`|`$output_method`|The output method. If 'echo', displays a list of topics, otherwise returns an array of info about them

### ssi_topTopicsViews

```php
function ssi_topTopicsViews(int $num_topics = 10, string $output_method = 'echo'): void|array
```
Top topics based on views



Type|Parameter|Description
---|---|---
`int`|`$num_topics`|How many topics to show
`string`|`$output_method`|The output method. If 'echo', displays a list of topics, otherwise returns an array of info about them

### ssi_latestMember

```php
function ssi_latestMember(string $output_method = 'echo'): void|array
```
Show a link to the latest member: Please welcome, Someone, our latest member.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', returns a string with a link to the latest member's profile, otherwise returns an array of info about them.

### ssi_randomMember

```php
function ssi_randomMember(string $random_type = '', string $output_method = 'echo'): void|array
```
Fetches a random member.



Type|Parameter|Description
---|---|---
`string`|`$random_type`|If 'day', only fetches a new random member once a day.
`string`|`$output_method`|The output method. If 'echo', displays a link to the member's profile, otherwise returns an array of info about them.

### ssi_fetchMember

```php
function ssi_fetchMember(array $member_ids = array(), string $output_method = 'echo'): void|array
```
Fetch specific members



Type|Parameter|Description
---|---|---
`array`|`$member_ids`|The IDs of the members to fetch
`string`|`$output_method`|The output method. If 'echo', displays a list of links to the members' profiles, otherwise returns an array of info about them.

### ssi_fetchGroupMembers

```php
function ssi_fetchGroupMembers(int $group_id = null, string $output_method = 'echo'): void|array
```
Get al members in the specified group



Type|Parameter|Description
---|---|---
`int`|`$group_id`|The ID of the group to get members from
`string`|`$output_method`|The output method. If 'echo', returns a list of group members, otherwise returns an array of info about them.

### ssi_queryMembers

```php
function ssi_queryMembers(string $query_where = null, array $query_where_params = array(), string|int $query_limit = '', string $query_order = 'id_member DESC', string $output_method = 'echo'): void|array
```
Pulls info about members based on the specified parameters. Used by other functions to eliminate duplication.



Type|Parameter|Description
---|---|---
`string`|`$query_where`|The info for the WHERE clause of the query
`array`|`$query_where_params`|The parameters for the WHERE clause
`string&#124;int`|`$query_limit`|The number of rows to return or an empty string to return all
`string`|`$query_order`|The info for the ORDER BY clause of the query
`string`|`$output_method`|The output method. If 'echo', displays a list of members, otherwise returns an array of info about them

### ssi_boardStats

```php
function ssi_boardStats(string $output_method = 'echo'): void|array
```
Show some basic stats:   Total This: XXXX, etc.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays the stats, otherwise returns an array of info about them

### ssi_whosOnline

```php
function ssi_whosOnline(string $output_method = 'echo'): void|array
```
Shows a list of online users:  YY Guests, ZZ Users and then a list.

..

Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a list, otherwise returns an array of info about the online users.

### ssi_logOnline

```php
function ssi_logOnline(string $output_method = 'echo'): void|array
```
Just like whosOnline except it also logs the online presence.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a list, otherwise returns an array of info about the online users.

### ssi_login

```php
function ssi_login(string $redirect_to = '', string $output_method = 'echo'): void|bool
```
Shows a login box



Type|Parameter|Description
---|---|---
`string`|`$redirect_to`|The URL to redirect the user to after they login
`string`|`$output_method`|The output method. If 'echo' and the user is a guest, displays a login box, otherwise returns whether the user is a guest

### ssi_topPoll

```php
function ssi_topPoll(string $output_method = 'echo'): void|array
```
Show the top poll based on votes



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays the poll, otherwise returns an array of info about it

### ssi_recentPoll

```php
function ssi_recentPoll(bool $topPollInstead = false, string $output_method = 'echo'): void|array
```
Shows the most recent poll



Type|Parameter|Description
---|---|---
`bool`|`$topPollInstead`|Whether to show the top poll (based on votes) instead of the most recent one
`string`|`$output_method`|The output method. If 'echo', displays the poll, otherwise returns an array of info about it.

### ssi_showPoll

```php
function ssi_showPoll(?int $topic = null, string $output_method = 'echo'): void|array
```
Shows the poll from the specified topic



Type|Parameter|Description
---|---|---
`null&#124;int`|`$topic`|The topic to show the poll from. If null, $_REQUEST['ssi_topic'] will be used instead.
`string`|`$output_method`|The output method. If 'echo', displays the poll, otherwise returns an array of info about it.

### ssi_pollVote

```php
function ssi_pollVote(): void
```
Handles voting in a poll (done automatically)



### ssi_quickSearch

```php
function ssi_quickSearch(string $output_method = 'echo'): void|string
```
Shows a search box



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a search box, otherwise returns the URL of the search page.

### ssi_news

```php
function ssi_news(string $output_method = 'echo'): void|string
```
Show a random forum news item



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', shows the news item, otherwise returns it.

### ssi_todaysBirthdays

```php
function ssi_todaysBirthdays(string $output_method = 'echo'): void|array
```
Show today's birthdays.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a list of users, otherwise returns an array of info about them.

### ssi_todaysHolidays

```php
function ssi_todaysHolidays(string $output_method = 'echo'): void|array
```
Shows today's holidays.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a list of holidays, otherwise returns an array of info about them.

### ssi_todaysEvents

```php
function ssi_todaysEvents(string $output_method = 'echo'): void|array
```
Shows today's events.



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a list of events, otherwise returns an array of info about them.

### ssi_todaysCalendar

```php
function ssi_todaysCalendar(string $output_method = 'echo'): void|array
```
Shows today's calendar items (events, birthdays and holidays)



Type|Parameter|Description
---|---|---
`string`|`$output_method`|The output method. If 'echo', displays a list of calendar items, otherwise returns an array of info about them.

### ssi_boardNews

```php
function ssi_boardNews(?int $board = null, ?int $limit = null, ?int $start = null, ?int $length = null, string $output_method = 'echo'): void|array
```
Show the latest news, with a template... by board.



Type|Parameter|Description
---|---|---
`null&#124;int`|`$board`|The ID of the board to get the info from. Defaults to $board or $_GET['board'] if not set.
`null&#124;int`|`$limit`|How many items to show. Defaults to $_GET['limit'] or 5 if not set.
`null&#124;int`|`$start`|Start with the specified item. Defaults to $_GET['start'] or 0 if not set.
`null&#124;int`|`$length`|How many characters to show from each post. Defaults to $_GET['length'] or 0 (no limit) if not set.
`string`|`$output_method`|The output method. If 'echo', displays the news items, otherwise returns an array of info about them.

### ssi_recentEvents

```php
function ssi_recentEvents(int $max_events = 7, string $output_method = 'echo'): void|array
```
Show the most recent events



Type|Parameter|Description
---|---|---
`int`|`$max_events`|The maximum number of events to show
`string`|`$output_method`|The output method. If 'echo', displays the events, otherwise returns an array of info about them.

### ssi_checkPassword

```php
function ssi_checkPassword(int|string $id = null, string $password = null, bool $is_username = false): bool
```
Checks whether the specified password is correct for the specified user.



Type|Parameter|Description
---|---|---
`int&#124;string`|`$id`|The ID or username of a user
`string`|`$password`|The password to check
`bool`|`$is_username`|If true, treats $id as a username rather than a user ID

### ssi_recentAttachments

```php
function ssi_recentAttachments(int $num_attachments = 10, array $attachment_ext = array(), string $output_method = 'echo'): void|array
```
Shows the most recent attachments that the user can see



Type|Parameter|Description
---|---|---
`int`|`$num_attachments`|How many to show
`array`|`$attachment_ext`|Only shows attachments with the specified extensions ('jpg', 'gif', etc.) if set
`string`|`$output_method`|The output method. If 'echo', displays a table with links/info, otherwise returns an array with information about the attachments

