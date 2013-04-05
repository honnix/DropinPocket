DropinPocket
============

Save URL to Pocket - Alfred Workflow

Converted from http://jdfwarrior.tumblr.com/post/21650256216/drop-in-pocket-extension-allows-you-to-quickly#_=_

To directly save url in current Safari tab into Pocket, you probably can compose following script (contributed by @bzzbzzz, please refer to https://github.com/honnix/DropinPocket/issues/1):

```
on alfred_script(q)
    set theTags to " " & q
    tell application "Safari" to set argForDropInPocket to URL of front document & theTags
    tell application "Alfred 2" to search "pocket" & " " & argForDropInPocket
end alfred_script
```

Or get the workflow [here](https://www.dropbox.com/s/9i5j0szz3hbvs0q/DropInPocket%2BSafari%2BSelection%2BClipboard.alfredworkflow). Can not guarantee availability of this file.