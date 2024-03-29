# macOS Setup

## Configuration

### Change Modifier Keys

System Preferences > Keyboard > Modifier Keys

```sequence
Caps Lock => Escape
Control => fn/Globe
Option => Option
Command => Command
fn/Globe => Control
```

### Application Shortcuts

System Preferences > Keyboard > Shortcuts > App Shortcuts > +

- All applications

```sequence
Close Tab => Control-w
Copy => Control-c
Paste => Control-v
```

- Google Chrome / Other Browswers

```sequence
New Tab => Control-t
```

### Mission Control (Workspace Switching)

System Preferences > Keyboard > Shortcuts > Mission Control

```sequence
Move left a space => Control-Command-Left Arrow
Move right a space => Control-Command-Right Arrow
```

## Shortcut for Opening a New Terminal on Current Desktop

### If You CAN Use Karibiber Elements

Copy the rule "Trigger Alacritty with CTRL-COMMAND-T" from the karabiner.json file in this repo
or simply copy/symlink the entire file into ~/.config/karabiner/karabiner.json

### If Can't Use Karibiner Elements
Create an `Automator` service

- Launchpad > Automator > File > New > Quick Action
- Change `Workflow receives current` dropdown to `no input`

_alacritty_

- Drag `Run Shell Script` to workflow box
- Enter the following command in text area

  ```
  /usr/local/bin/alacritty </dev/null &>/dev/null &
  ```

_default terminal_

- Drag `Run AppleScript` to workflow box
- Enter the following command in text area

  ```
  tell application "Terminal"
    do script ""
    activate
  end tell
  ```

- Save the quick action: File > Save (with name like AutomatorActionName)
- Set the keyboard shortcut: System Preferences > Keyboard > Shortcuts > Services > General > AutomatorActionName

## Applications

> A note on homebrew installations:

If you are getting a SHA-256 mismatch:

- Remove downloaded .gz / .zip file from cache directory

```sequence
brew --cache packagename
```

- Download matching release from githuub
- Overwrite downloaded file from github to cache using `mv`
- Install via

```sequence
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

```sequence
brew edit vim
```

2.

```sequence
system "./configure", "--prefix=#{HOMEBREW_PREFIX}",
                      "--mandir=#{man}",
                      "--enable-multibyte",
                      "--with-features=huge",
```

3.

```sequence
brew install --build-from-source vim
brew link vim
```

### Rectangle (Window Tiling)

- Remap tile-left, tile right, tile right-top ... etc

```sequence
brew install --cask rectangle
```

### Jumpcut (Optional)

- Tracks clipboard history

```sequence
brew install --cask jumpcut
```

### Alt-Tab

- Use <alt-tab> to cycle windows, whereas mac native cycles by applications

```sequence
brew install --cask alt-tab
```

_Preferences_

- Keybinding: `<alt-tab>`
- Minimized Windows: Hide
- Hidden Windows: Hide

### Tree

```sequence
brew install tree
```

### Browser Extensions

- surfingkeys https://github.com/tecfu/Surfingkeys/tree/hack_hint_sizes
  - Best known vim plugin (> vimium, > vimium-c)
- Duplicate Tab: https://github.com/stefansundin/duplicate-tab
