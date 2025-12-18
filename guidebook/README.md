# Guidebook Sync

sync_guidebook will update our Guidebook account based on a CSV file.

## Resources

* [Guidebook API docs](https://developer.guidebook.com/)

NOTE: This script assumes you have already uploaded the main map manually
(included in this repo).

## Source

To get the source CSV file, visit
[https://www.socallinuxexpo.org/admin/export/23x/sessions](https://www.socallinuxexpo.org/admin/export/23x/sessions)
as an admin (change `23x` to your year).

## Authentication

You can get a Guidebook API [in your
account](https://builder.guidebook.com/#/account/api/).

Put it in a file and pass it to `-a`.

If you are doing regioned-maps, you will need to have an "internal" API key.
Log into guidebook, and then open a developer console and shove in:

```javascript
alert(JSON.parse(('; '+document.cookie).split(`; CurrentUser=`).pop().split(';')[0]).jwt)
```

Put that in a file and pass it to `-x`.
