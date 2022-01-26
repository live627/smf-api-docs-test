---
layout: default
group: func
navtitle: Agreement.php
title: ./Sources/Agreement.php
count: 5
---
* auto-gen TOC:
{:toc}
### prepareAgreementContext

```php
/*	The purpose of this file is to show the user an updated registration
	agreement, and get them to agree to it.

	bool prepareAgreementContext()
		// !!!

	bool canRequireAgreement()
		// !!!

	bool canRequirePrivacyPolicy()
		// !!!

	void Agreement()
		- Show the new registration agreement

	void AcceptAgreement()
		- Called when they actually accept the agreement
		- Save the date of the current agreement to the members database table
		- Redirect back to wherever they came from
*/
function prepareAgreementContext()
```
### canRequireAgreement

```php
function canRequireAgreement()
```
### canRequirePrivacyPolicy

```php
function canRequirePrivacyPolicy()
```
### Agreement

```php
// Let's tell them there's a new agreement
function Agreement()
```
### AcceptAgreement

```php
// I solemly swear to no longer chase squirrels.
function AcceptAgreement()
```
