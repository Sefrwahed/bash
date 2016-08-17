---
layout: main
title: Process Management
---
# Process Management

## Managing Jobs

### `jobs`

* Lists all the running processes/jobs with its status
* The jobs with `+` is the job with focus, so if you call `bg` or `fg` without arguments this job will catch the command

### `bg`

* Sends an inactive process/job to work in the background
* example: `bg 1` brings job 1 to work in foreground

### `fg`

* Brings the background process to the foreground
* example: `fg 2` brings job 2 to work in foreground

### `&`

* Allows you to create and send the process to the background
* example: `sleep 10 &` will create a sleeping process and let it work in the background

> Note: `CTRL+Z` makes the current process/job inactive you can call `bg` to let it run in the background or `fg` to let it run in the foreground

## Monitoring Jobs

### `ps`

* List the processes running on the current shell session
* example: `ps` to list processes you can add options `-l` or `-f` for more details
* exmaple: `ps -e` will list all the processes on the system

### `pgrep`

* List PID for a specific name of program or service
* example: `pgrep chromium` list all process id for Chromium app

## Killing Jobs

### `kill`

* Terminates a process using its PID
* example: `kill 18999` will kill the process with id 18999
* The default signal sent is `SIGTERM` for terminate
* There are some other signals use `kill -l` to list them
* Some processes do not respond to `SIGTERM` you have to send a more powerful signal
* example: `kill -kill <pid>` or `kill -sigkill <pid>` or `kill -9 <pid>`

### `pkill`

* Terminates the process using the name
* example: `sleep 20 &` and `pkill sleep` this will terminate the sleep command

### `killall`

* Just like pkill you can specify the name of the program to kill all instances

## Process Manager

### `top`

* Just like Windows task manage but runs in the terminal
* You can see all running processes and their children
* You can also terminate whatever you want
* You can specify number of captures using `-n` and also specify a delay before each capture using `-d`
* There is a third party fork of `top` called `htop` it has a better UI