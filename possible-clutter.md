# Possible Clutter

Some folders/apps that clutter on macos.

## Apple Voice Memos
When everything is synced to iCloud, this can be a multi GB folder, you can savely delete:
`~/Library/Application Support/Group Containers/group.com.apple.VoiceMemos.shared`

## node_modules
If you develop javascript stuff these can clutter a huge portion of your system.
Use `find . -type d -name node_modules -prune 2>/dev/null` to get the node_modules folders in the current dictonary. `-prune` stops find from going into subfolders inside node_modules.
Checking the whole system often was not helpful, as many electron apps also have a node_modules folder that is needed for them to function.

To be continued…
