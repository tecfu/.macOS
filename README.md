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

Create an `Automator` service
  - Launchpad > Automator > File > New > Quick Action
  - Change `Workflow receives current` dropdown to `no input`
  - Drag `Run Shell Script` to workflow box
  - Change `Shell` dropdown to `/bin/bash`
  - Enter the following command in text area
      ```
      open -a Terminal ~/Documents/Github
      ```
  - Save the quick action with a yourActonName
  - Set the keyboard shortcut: System Preferences > Keyboard > Shortcuts > Services > General > yourActonName

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


- vimium-c https://github.com/gdh1995/vimium-c
    - Better scrolling of modals out-of-the-box (vimium fails at this)
- Duplicate Tab: https://github.com/stefansundin/duplicate-tab
