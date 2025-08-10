# Possible Clutter

## Apps / Folders
Some folders/apps that clutter on macos.

### Apple Voice Memos
When everything is synced to iCloud, this can be a multi GB folder, you can savely delete:
`~/Library/Application Support/Group Containers/group.com.apple.VoiceMemos.shared`

### node_modules
If you develop javascript stuff these can clutter a huge portion of your system.
Use `find . -type d -name node_modules -prune 2>/dev/null` to get the node_modules folders in the current dictonary. `-prune` stops find from going into subfolders inside node_modules.
Checking the whole system often was not helpful, as many electron apps also have a node_modules folder that is needed for them to function.

To be continued…

## Terminal Stuff

To get the folders in your current dictonary listed sorted by size, use `du`.
Here is a full command is use: `du -h -d 1 -t 2M | sort -hr`. This also only gets the folders over 2mb.
Use `du -sh *` to get the size of all direct subfolders without sorting or restrictions.

Find folders by using something like `find . -type d -name "node_modules" 2>/dev/null`. (`2>/dev/null` makes it ignore all errors.)

Use `rm -R your_folder_path` to delete whole dictonaries. PLEASE be careful!!! This deletes stuff without being able to bring it back.

## Articles about cleaning storage space on macos

[What is safe to delete?](https://daisydiskapp.com/guide/what-to-delete)

Something about `DARWIN_USER_CACHE_DIR`: [The missing gigabytes of disk space on my Mac](https://www.ctrl.blog/entry/darwin-user-cache-gigabytes.html)
