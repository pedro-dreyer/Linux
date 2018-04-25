# Linux

## SSH

- **Enable X11 port fowarding:** Connect using `ssh -X name@server` to make the terminal have X11 port fowarding. This makes among other things vim to have acess to the clipboard and that programs opened in the host machine to appear in the local machine.

## VIM

- **Clipboard acess:** To have acess to the clipboard VIM needs to have the xterm\_cipboard option enabled. One package which has this enabled is vim-gnome. youcan install it using the command `sudo apt-get install vim-gnome`.

- **Open terminal output** To open a terminal output we need to pass the `-` option e.g. `man tmux | vim -`

## MISC

- **Copy/Paste:** We can copy with <kbd>Ctrl</kbd>+<kbd>Insert</kbd> and paste with <kbd>Shift</kbd>+<kbd>INSERT</kbd> in most linux applications.

## TMUX
- To force a 256 color terminal put `set -g default-terminal 'tmux-256color'` in `.tmux.conf`


## SHELL/TERMINAL

## FZF
