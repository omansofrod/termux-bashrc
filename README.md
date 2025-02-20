### bashrc ###
### storage cleaner ###
```
alias xdx="while :; do echo ''>>1 | echo ''>>2 | echo ''>>3 | echo ''>>4 | echo ''>>5 | echo ''>>6 | echo ''>>7 | echo ''>>8 | echo ''>>9 | echo ''>>0 | cat 0 >> 1 | cat 1 >> 2 | cat 2 >> 3 | cat 3 >> 4 | cat 4 >> 5 | cat 5 >> 6 | cat 6 >> 7 | cat 7 >> 8 | cat 8 >> 9 | cat 9 >> 0 ;clear ;done"
alias xdr="clear; touch 0; rm -v 0 && rm -v 1 && rm -v 2 && rm -v 3 && rm -v 4 && rm -v 5 && rm -v 6 && rm -v 7 && rm -v 8 && rm -v 9"
alias xdl="while :; do ls -la; df /sdcard/;df /storage/3938-3131; clear; done"
alias xds="shred -vf 0 | shred -vf 1 | shred -vf 2 | shred -vf 3 | shred -vf 4 | shred -vf 5 | shred -vf 6 | shred -vf 7 | shred -vf 8 | shred -vf 9"
alias xdsr="shred -uvf 0 | shred -uvf 1 | shred -uvf 2 | shred -uvf 3 | shred -uvf 4 | shred -uvf 5 | shred -uvf 6 | shred -uvf 7 | shred -uvf 8 | shred -uvf 9"
```
### storage path ###
```
alias sd="clear; cd /sdcard/; ls -1"
alias se="clear; cd ~/; ls -1"
alias sx="clear; cd /storage/3938-3131; ls -1"
alias sf="clear; cd /data/data/com.termux/files/; ls -1"
alias su="clear; cd $PREFIX/; ls -1"
```
### simpleusualy ###
```
alias ll="clear; ls -la"
alias l="clear; ls -1a"
del && clear && echo clear
```

### termux.properties ###
![Image](https://github.com/user-attachments/assets/cca4a935-2966-4fea-9a6c-4befbc600a2c)
```
### This is a `.properties` [https://en.wikipedia.org/wiki/.properties] file
### for termux app properties and is loaded with the `java.util.Properties.load()`
### [https://developer.android.com/reference/java/util/Properties#load(java.io.Reader)]
### call by the termux app and must be formatted as per its spec.
### To make changes to a property value, uncomment the property line by removing
### any hash `#` characters at the start of the line.
### After making required changes, save the file and run `termux-reload-settings`
### in the terminal for changes to take effect. Some properties require app
### process to be restarted to be updated which can be done by force stopping
### the app from Android app settings.
### All information here can also be found on the
### wiki: https://wiki.termux.com/wiki/Terminal_Settings

###############
# General
###############

### Allow external applications to execute arbitrary commands within Termux.
### This potentially could be a security issue, so option is disabled by
### default. Uncomment to enable.
# allow-external-apps = true

### Default working directory that will be used when launching the app.
# default-working-directory = /data/data/com.termux/files/home

### Uncomment to disable toasts shown on terminal session change.
# disable-terminal-session-change-toast = true

### Uncomment to not show soft keyboard on application start.
# hide-soft-keyboard-on-startup = true

### Uncomment to let keyboard toggle button to enable or disable software
### keyboard instead of showing/hiding it.
# soft-keyboard-toggle-behaviour = enable/disable

### Adjust terminal scrollback buffer. Max is 50000. May have negative
### impact on performance.
# terminal-transcript-rows = 2000

### Uncomment to use volume keys for adjusting volume and not for the
### extra keys functionality.
# volume-keys = volume

###############
# Fullscreen mode
###############

### Uncomment to let Termux start in full screen mode.
# fullscreen = true

### Uncomment to attempt workaround layout issues when running in
### full screen mode.
# use-fullscreen-workaround = true

###############
# Cursor
###############

### Cursor blink rate. Values 0, 100 - 2000.
 terminal-cursor-blink-rate = 123

### Cursor style: block, bar, underline.
 terminal-cursor-style = bar

###############
# Extra keys
###############

### Settings for choosing which set of symbols to use for illustrating keys.
### Choose between default, arrows-only, arrows-all, all and none
# extra-keys-style = default

### Force capitalize all text in extra keys row button labels.
# extra-keys-text-all-caps = true

### Default extra-key configuration
# extra-keys = [[ESC, TAB, CTRL, ALT, {key: '-', popup: '|'}, DOWN, UP]]

### Two rows with more keys
# extra-keys = [['ESC','/','-','HOME','UP','END','PGUP'], \
#               ['TAB','CTRL','ALT','LEFT','DOWN','RIGHT','PGDN']]

### Configuration with additional popup keys (swipe up from an extra key)
# extra-keys = [[ \
#   {key: ESC, popup: {macro: "CTRL f d", display: "tmux exit"}}, \
#   {key: CTRL, popup: {macro: "CTRL f BKSP", display: "tmux ←"}}, \
#   {key: ALT, popup: {macro: "CTRL f TAB", display: "tmux →"}}, \
#   {key: TAB, popup: {macro: "ALT a", display: A-a}}, \
#   {key: LEFT, popup: HOME}, \
#   {key: DOWN, popup: PGDN}, \
#   {key: UP, popup: PGUP}, \
#   {key: RIGHT, popup: END}, \
#   {macro: "ALT j", display: A-j, popup: {macro: "ALT g", display: A-g}}, \
#   {key: KEYBOARD, popup: {macro: "CTRL d", display: exit}} \
# ]]

### Another configuration with advanced popup key usage designed for more
### specific use-cases. In this case, it is designed for working with Vim-like
### editors for faster navigation
#extra-keys = [ \
#  [ \
#    { key: ESC, popup: { macro: ":q\n", display: "QuickExit" } }, \
#    { key: '/', popup: '\\\\' }, \
#    { key: '-', popup: '_' }, \
#    { key: HOME, popup: { macro: "CTRL HOME", display: "Top" } }, \
#    { key: UP, popup: { macro: "CTRL UP", display: "UP" } }, \
#    { key: END, popup: { macro: "CTRL END", display: "End" } }, \
#    { key: ":", popup: ";" }, \
#    { key: "(", popup: "{" } \
#  ], \
#  [ \
#    { key: TAB, popup: { macro: ":wq\n", display: "Write And Exit" } }, \
#    { key: CTRL, popup: { macro: ":w\n", display: "Write" } }, \
#    ALT, \
#    { key: LEFT, popup: { macro: "CTRL LEFT", display: "Left" } }, \
#    { key: DOWN, popup: { macro: "CTRL DOWN", display: "Bottom" } }, \
#    { key: RIGHT, popup: { macro: "CTRL RIGHT", display: "Right" } }, \
#    { key: "#", popup: "$" }, \
#    { key: ")", popup: "}" } \
#  ] \
#]

###############
# Colors/themes
###############

### Force black colors for drawer and dialogs
# use-black-ui = true

###############
# HW keyboard shortcuts
###############

### Disable hardware keyboard shortcuts.
# disable-hardware-keyboard-shortcuts = true

### Open a new terminal with ctrl + t (volume down + t)
# shortcut.create-session = ctrl + t

### Go one session down with (for example) ctrl + 2
# shortcut.next-session = ctrl + 2

### Go one session up with (for example) ctrl + 1
# shortcut.previous-session = ctrl + 1

### Rename a session with (for example) ctrl + n
# shortcut.rename-session = ctrl + n

###############
# Bell key
###############

### Vibrate device (default).
# bell-character = vibrate

### Beep with a sound.
# bell-character = beep

### Ignore bell character.
# bell-character = ignore

###############
# Back key
###############

### Send the Escape key.
# back-key=escape

### Hide keyboard or leave app (default).
# back-key=back

###############
# Keyboard issue workarounds
###############

### Letters might not appear until enter is pressed on Samsung devices
# enforce-char-based-input = true

### ctrl+space (for marking text in emacs) does not work on some devices
# ctrl-space-workaround = true
```
### adb ###
