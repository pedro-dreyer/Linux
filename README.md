# Linux

## SSH

- **Enable X11 port fowarding:** Connect using `ssh -X name@server` to make the terminal have X11 port fowarding. This makes among other things vim to have acess to the clipboard and that programs opened in the host machine to appear in the local machine.

## VIM

- **Clipboard acess:** To have acess to the clipboard VIM needs to have the xterm\_cipboard option enabled. One package which has this enabled is vim-gnome. youcan install it using the command `sudo apt-get install vim-gnome`.

- **Open terminal output** To open a terminal output we need to pass the `-` option e.g. `man tmux | vim -`

## MISC

- **Copy/Paste:** We can copy with <kbd>Ctrl</kbd>+<kbd>Insert</kbd> and paste with <kbd>Shift</kbd>+<kbd>Insert</kbd> in most linux applications.

## TMUX

- **256 colors:** We must put the following lines in `.tmux.conf` 

```shell
set -g default-terminal 'tmux-256color'
set -as terminal-overrides ',xterm*:Tc:sitm=\E[3m'
```
- **tmux-256color not fount:** For some reason one of my machines dosn't have `tmux-256color` so we need to send it from another machine which has it and then compile it.

Machine with `tmux-256color.ti`
```shell
$ infocmp tmux-256color > tmux-256color.ti
$ scp -r tmux-256color.ti name@server:~/
```
Machine without `tmux-256color.ti`
```shell
$ tic tmux-256color.ti
```
this will create some files in the `.terminfo` folder that will correct render the terminal colors
## FZF

## SHELL/TERMINAL
