---
layout: main
title: Command line Pipes
---

# Command line pipes

Write input from one command to a file or passing the output to another command as an input

## Redirection

### Write to a file `>`

* Writes the output to a file
* If the file exists it will overwrite its content
* If file does not exist it will create it and add content to it

**Note:**

* there is a command to prevent overwriting files: `set -o noclobber`
* there is `>|` operator to ignore the `noclobber` command

### Append to a file `>>`

* Does exactly like the `>`
* but instead it appends the output to the existing content of the file

### Redirecting standard output and error

* By default `>` is equivalent to `1>`
* The symbol `1>` means redirect standard output
* If we are interested in errors produced by command we use `2>`
* example: `ls non-existing-folder/ 2> out.txt`
* If we are interested in saving both output and error we use `2>&1` which means **redirect** standard error to the same place of standard output
* If you are not interested in anything you can use `/dev/null`
* example: `ls /dir1 /dir2 > /dev/null 2>&1`

### Read from file `<`

Nothing interesting in my mind now

## Pipelines

### Unnamed pipelines `|`

* Simply you can take the output from some command and give to another
* example: `cut -f 1 -d ',' f.csv | sort`

### Named pipelines using `mkfifo`

* Create a pipe to use from anywhere
* example: `mkfifo sefrwahed` `ls > sefrwahed` `wc -l < sefrwahed`