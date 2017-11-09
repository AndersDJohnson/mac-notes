# mac-notes
Mac notes. A.K.A. OS X, macOS.

## See Also
* [unix-notes][unix-notes]
* [windows-notes][windows-notes]
* [dotfiles](https://github.com/AndersDJohnson/dotfiles)
  * [install-mac.sh](https://github.com/AndersDJohnson/dotfiles/blob/master/install-mac.sh)
* [applescripts](https://github.com/AndersDJohnson/applescripts)

## Hotkeys

See also:
* https://support.apple.com/en-us/HT201236

Key | Symbol
--- | ---
Command | `⌘`
Option | `⌥`
Control | `⌃`
Shift | `⇧`
Caps Lock | `⇪`

Name | Hotkey
--- | ---
Lock screen | `^` `⇧` `Esc` or `^` `⇧` `Power`
Help menu search | `⌘` `⇧` `/`
Screenshot (full) | `⌘` `⇧` `3`
Screenshot (part) | `⌘` `⇧` `4`
Screenshot (window) | `⌘` `⇧` `4` `Space`
Force Quit apps | `⌘` `⌥` `Esc`
Force Quit current app | `⌘` `⌥` `⇧` `Esc`
Show hidden files | `⌘` `⇧` `.`

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

## Software Update

### Fix stuck
```
softwareupdate -i -a
```

## Longer notifications

http://osxdaily.com/2014/01/29/change-notifications-banner-time-mac-os-x/

```
defaults write com.apple.notificationcenterui bannerTime 100
```

reset:
```
defaults delete com.apple.notificationcenterui bannerTime
```

## Full Keyboard Access

Enable this.

> With Full Keyboard Access, you use the Tab key and arrow keys to navigate to items on the screen, and the Space bar to select an item.

https://support.apple.com/en-us/HT204434

## Change screenshot location

```
defaults write com.apple.screencapture location ~/Pictures/Screenshots
```
then:
```
killall SystemUIServer
```
