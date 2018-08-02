# Linux

## MISC

- **Terminal in vi mode:** `set -o vi`

  https://unix.stackexchange.com/questions/4870/is-it-possible-to-have-vim-key-bindings-in-terminal
  http://www.catonmat.net/blog/bash-vi-editing-mode-cheat-sheet/

- **find where command is located:** `which command` 

- **alliases to commands:** `alias short_command='long command'`

- **Make a script executable:** `chmod +x filename.sh`

- **Environment variables:** 

  \- Set environment variables: `export NEW_VAR="new variable"`  
  \- Print environment variables: `printenv`  
  \- Pass a environment variable to a program: `env NEW_VAR='value' command_to_run command options`  
  \- Add environment variable to .bashrc: `echo export NEW_VAR='new variable' >> ~/.bashrc`

- **Copy/Paste:** We can copy with <kbd>Ctrl</kbd>+<kbd>Insert</kbd> and paste with <kbd>Shift</kbd>+<kbd>Insert</kbd> in most linux applications. Other means are also <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>c</kbd> and <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>v</kbd> for copying and pasting, and pressing the middle or the left and right mouse buttons for pasting. 

- **Migrate users from one linux installation to another:**

   * Copy the lines corresponding to the users you want to migrate, from the files `/etc/shadow`, `/etc/group` and `/etc/passwd`.
   * Paste then in the corresponding files in the new system.
   * Copy the users `/home/` folder.
   * It could be necessary to change the permission of the home folders. Do that with the command `sudo chown -R username:group directory`.

  https://serverfault.com/questions/19274/how-to-transfer-user-accounts-to-a-new-linux-machine

  https://askubuntu.com/questions/6723/change-folder-permissions-and-ownership

- **Create Users:** Use the command `sudo adduser new_username`

  https://askubuntu.com/questions/410244/a-command-to-list-all-users-and-how-to-add-delete-modify-user
  
- **Limit memory usage per user:** edit the file /etc/security/limits.conf and add `'username' as hard 'memlimit'`

 http://shortrecipes.blogspot.com/2009/04/limitsconf-virtual-memory-limit.html


## SSH

- **Enable X11 port fowarding:** Connect using `ssh -X name@server` to make the terminal have X11 port fowarding. This makes among other things vim to have acess to the clipboard and that programs opened in the host machine to appear in the local machine.

## VIM

- **Clipboard acess:** To have acess to the clipboard VIM needs to have the xterm\_cipboard option enabled. One package which has this enabled is vim-gnome. youcan install it using the command `sudo apt-get install vim-gnome`.

- **Open terminal output** To open a terminal output we need to pass the `-` option e.g. `man tmux | vim -`

  https://serverfault.com/questions/19274/how-to-transfer-user-accounts-to-a-new-linux-machine

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

## PASS

## GPG

## INSTALLED PROGRAMS

- MyPaint
- Pass
- Gnupg [1](ttps://wiki.archlinux.org/index.php/GnuPG#Unattended_passphrase)
- Grip


