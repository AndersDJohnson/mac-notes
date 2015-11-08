# mac-notes
Mac notes. A.K.A. OS X.

See also:
* [AndersDJohnson/dotfiles](https://github.com/AndersDJohnson/dotfiles)
  * [install-mac.sh](https://github.com/AndersDJohnson/dotfiles/blob/master/install-mac.sh)
* [AndersDJohnson/applescripts](https://github.com/AndersDJohnson/applescripts)

## Hotkeys

See also:
* https://support.apple.com/en-us/HT201236

Name | Hotkey
--- | ---
Help menu search | (⌘)-Shift-/
Screenshot (full) | (⌘)-Shift-3
Screenshot (part) | (⌘)-Shift-4
Screenshot (window) | (⌘)-Shift-4 Space

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
sudo dseditgroup -o edit -a usernametoadd -t user admin
```
