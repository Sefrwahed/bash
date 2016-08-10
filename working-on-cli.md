---
layout: main
title: Working on CLI
---

# Working on CLI

## Access terminals

### Physical consoles

* Normally we have from tty1 to tty6
* We use `CTRL + ALT + F#` or `chvt #` command

### Pseudo Consoles

* Created through GUI, Telnet, or SSH
* Most common
* Created dynamically in `/dev/pts/`

## Identify connected terminal

* To view my current console we use `tty` command
* To list logins on the machine we use `who` command
* If the connection is remote we use environment variables $SSH_
* BASH is not the only shell, try `chsh -l` to see the rest
* Your default shell is configured in `/etc/passwd`

## Bash history

* Your command history is stored in `~/.bash_history`
* `!v` will run the last command starting with **v**
* `!$` represents the last argument
* `!?etc` will run the last command containing **etc**
* `CTRL + r` will start reverse search, and you can re-execute it
* `history` command views the recent commands

## EXTRA: Installing ZSH

* If you are on Ubuntu you can do `sudo apt-get install zsh`
* Change you shell using `chsh -s /usr/bin/zsh`
* go to `http://ohmyz.sh` and follow instruction to get a fancy terminal