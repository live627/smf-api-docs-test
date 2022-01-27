---
layout: default
group: hooks
title: PackageGet.php
count: 3
---
* auto-gen TOC:
{:toc}
### integrate_package_get

```php
call_integration_hook('integrate_package_get', array(&$subActions))
```

Type|Parameter|Description
---|---|---
`array`|`$&subActions`|desc

Called from
: [`PackageGet()` in `./Sources/PackageGet.php`](../docs/packageget.html#packageget)

Notes
: Since 2.1

### integrate_package_download

```php
call_integration_hook('integrate_package_download')
```


Called from
: [`PackageDownload()` in `./Sources/PackageGet.php`](../docs/packageget.html#packagedownload)

Notes
: Since 2.1

### integrate_package_upload

```php
call_integration_hook('integrate_package_upload')
```


Called from
: [`PackageUpload()` in `./Sources/PackageGet.php`](../docs/packageget.html#packageupload)

Notes
: Since 2.1

