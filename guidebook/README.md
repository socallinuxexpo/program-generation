sync_guidebook will update our Guidebook account based on a CSV file.

Find docs here:
https://developer.guidebook.com/

Find a key here:
https://builder.guidebook.com/#/account/api/

If you are doing regioned-maps, you will need to have an "internal" API key. Log into guidebook, and then open a developer console and shove in:

```
alert(JSON.parse(('; '+document.cookie).split(`; CurrentUser=`).pop().split(';')[0]).jwt)
```

put that in a file and pass it to `-x`
