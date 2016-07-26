# mac-notes
Mac notes. A.K.A. OS X.

## See Also
* [AndersDJohnson/unix-notes][unix-notes]
* [AndersDJohnson/windows-notes][windows-notes]
* [AndersDJohnson/dotfiles](https://github.com/AndersDJohnson/dotfiles)
  * [install-mac.sh](https://github.com/AndersDJohnson/dotfiles/blob/master/install-mac.sh)
* [AndersDJohnson/applescripts](https://github.com/AndersDJohnson/applescripts)

## Hotkeys

See also:
* https://support.apple.com/en-us/HT201236

Key | Symbol
--- | ---
Command | `⌘`
Shift | `⇧`
Option | `⌥`
Control | `⌃`
Caps Lock | `⇪`

Name | Hotkey
--- | ---
Lock screen | `^` `⇧` `Esc` or `^` `⇧` `Power`
Help menu search | `⌘` `⇪` `/`
Screenshot (full) | `⌘` `⇪` `3`
Screenshot (part) | `⌘` `⇪` `4`
Screenshot (window) | `⌘` `⇪` `4` `Space`
Force Quit apps | `⌘` `⌥` `Esc`
Force Quit current app | `⌘` `⌥` `⇧` `Esc`

## Users & Groups

### Create Group

First check:
```
sudo dscl . -read /Groups/mysql
```

Then create:
```
sudo dscl . -create /Groups/mysql gid 296
```

http://serverfault.com/a/171619

### Add User to Group
```
sudo dseditgroup -o edit -a $USERNAME -t user $GROUP
```

[unix-notes]: https://github.com/AndersDJohnson/unix-notes
[windows-notes]: https://github.com/AndersDJohnson/windows-notes

## Networking

### Default Gateway
```
route -n get default
```
