# DropinPocket

Save URL to Pocket - Alfred Workflow

Converted from http://jdfwarrior.tumblr.com/post/21650256216/drop-in-pocket-extension-allows-you-to-quickly#_=_

To directly save url in current Safari tab into Pocket, you probably can compose following script (contributed by @bzzbzzz, please refer to [#1](https://github.com/honnix/DropinPocket/issues/1)):

```
on alfred_script(q)
    set theTags to " " & q
    tell application "Safari" to set argForDropInPocket to URL of front document & theTags
    tell application "Alfred 2" to search "pocket" & " " & argForDropInPocket
end alfred_script
```

Or get the workflow [here](https://www.dropbox.com/s/9i5j0szz3hbvs0q/DropInPocket%2BSafari%2BSelection%2BClipboard.alfredworkflow). Can not guarantee availability of this file.

## Note for v3

After migrating to v3 API, authentication should be oauth, and currently I don't have time to fix redirect_uri, you need
to fix it by yourselves.

1. pocket setup (Safari will be launched, and there you need to sign in with your Pocket username/pwd, after that you might be redirected to project's github page, just ignore that)
2. pocket auth (your access token will be recorded to a file under the directory of this workflow, sorry it is not encrypted)
3. then you are ready to go