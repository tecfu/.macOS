# macOS Setup


## Configuration

### Change Modifier Keys

System Preferences > Keyboard > Modifier Keys

```
Caps Lock => Escape
Control => fn/Globe
Option => Option
Command => Command
fn/Globe => Control
```


### Application Shortcuts

System Preferences > Keyboard > Shortcuts > App Shortcuts > +


- All applications
```
Close Tab => Control-w
New Tab => Control-t
Copy => Control-c
Paste => Control-v
````
### Mission Control (Workspace Switching)

System Preferences > Keyboard > Shortcuts > Mission Control

```
Move left a space => Control-Command-Left Arrow
Move right a space => Control-Command-Right Arrow
```

## Shortcuts for Opening Applications


- Setup various applications to open on keyboard shortcut

```
Launchpad > Shortcuts > File > New Shortcut
Open Application
Type Name of Application
Details icon (top right) > Run With
```
Remember to blur the input box in order for the shortcut to save.


- Setup terminal to open in new window on keyboard shortcut

```
Launchpad > Shortcuts > File > New Shortcut
Enter Shortcut Name
Apps > Terminal > Run Shell Script
```

Then for the shell script enter:

```
open -a Terminal ~/Documents
```

Then set the keyboard shortcut. 

```
Details icon (top right) > Run With
```
Remember to blur the input box in order for the shortcut to save.


## Applications

> A note on homebrew installations:
 
 If you are getting a SHA-256 mismatch:

 - Remove downloaded .gz / .zip file from cache directory
 ```
 brew --cache packagename
 ```
 - Download matching release from githuub
 - Overwrite downloaded file from github to cache using `mv`
 - Install via
 ```
 brew upgrade packagename
 ```


### Slack

Make sure Slack notifications are on
System Preferences > Sounds and Notifications > Slack > Enable


### Git

- Git autocomplete in terminal
https://www.macinstruct.com/tutorials/how-to-enable-git-tab-autocomplete-on-your-mac/


## Installations

### Vim 

1.
```
brew edit vim
```

2.
```
system "./configure", "--prefix=#{HOMEBREW_PREFIX}",
                      "--mandir=#{man}",
                      "--enable-multibyte",
                      "--with-features=huge",
```

3.
```
brew install --build-from-source vim
brew link vim
```


### Rectangle (Window Tiling) 
- Remap tile-left, tile right, tile right-top ... etc

```
brew install --cask rectangle
```

### Jumpcut (Optional)

- Tracks clipboard history

```
brew install --cask jumpcut
```

### Alt-Tab
- Use <alt-tab> to cycle windows, whereas mac native cycles by applications
```
brew install --cask alt-tab
```

*Preferences*

- Keybinding: `<alt-tab>`
- Minimized Windows: Hide
- Hidden Windows: Hide


### Tree
```
brew install tree
```


### Browser Extensions


- Vimium
- Duplicate Tab: https://github.com/stefansundin/duplicate-tab
