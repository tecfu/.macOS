# macOS Configuration 


## Keyboard Shortcuts

### Change Modifier Keys

System Preferences > Keyboard > Modifier Keys

```
Caps Lock => Escape
Control => fn
Option => Option
Command => Command
fn => Control
```


### Application Shortcuts

System Preferences > Keyboard > Shortcuts > App Shortcuts > +


- All applications
```
Close Tab => Control-W
New Tab => Control-T
```

### Mission Control (Workspace Switching)

System Preferences > Keyboard > Shortcuts > Mission Control

```
Move left a space => Control-Command-Left Arrow
Move right a space => Control-Command-Right Arrow
```


## Rectangle (Window Tiling) 

```
brew install --cask rectangle
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




