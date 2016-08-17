---
layout: main
title: Basic File Management
---

# Basic File Management

## Toolbox

### `ls`

* Used for listing directories
* example: `ls folder1` this will list the contents of `folder1`
* There is an option `-R` to a recursive listing
* example: `ls -R folder1` this will list the contents of `folder1` and all its children folders

### `cp`

* Used for copying file and directories
* example: `cp file1 file2` this will get you a copy of `file1` with the name `file2`
* There is a useful option `-i` to activate the interactive mode
* example: `cp -i file1 file2` if `file2` already existing it will ask you if you would like to overwrite it
* The `-R` option is applicable here too

### `mv`

* Used for moving or renaming files directories
* example: `mv foo bar` this will rename the file `foo` to `bar` unless `bar` is a directory, If bar is a directory, the file `foo` will be moved to it
* The `-R` and `-i` are applicable here to

### `rm` and `rmdir`

* Use `rm` to delete file **permanently** from disk
* example: `rm file1` to delete the file
* example: `rm -i f*` will delete all files staring with **f** and the `-i` will ask you before deleting each
* Use `rmdir` command to delete **empty** directories only
* To delete non-empty directories use `rm -rf dirname`, the `-rf` option means **recursive** deletion with **forcing**, **USE WITH CAUTION**

### `ls`

* We already know that `ls` is used for listing directories
* The `-l` will provide you a detailed list, you can also add `-h` option to get a human readable format
* The `-t` will sort by the modification date, you can also add `-r` to reverse the listing
* If coloring is turned off on your machine you can turn it on with `--color=auto` option
* Of course there is a bunch of options for `ls`. Use `ls --help` to explore them

> NOTE: If you have a command like this `ls -l -h` you can shorten it to `ls -lh` and get the same result

### `find`

* Allows you to find files or directories efficiently
* The `-newer` option allows you to find files newer than a specific file
* example: `find . -newer file1` will get you all files and folders create after `file1`


* You can invert and option using `!` operator
* example: `find . ! -newer file1` will get you all files and folders older than `file1`


* You can also use `-delete` option to delete all found files
* example: `find -newer file1 -delete` this will delete all files newer than `file1`


* There is the option `-type` which allows you to specify the file type `f` for regular files and `d` for directories


* The option `-name` with a name or a pattern allows you to find files/folders with specific name
* example: `find . -name '*.pdf'` will get all pdf files in current directory


* The option `-maxdepth` with a number allows to specify the depth of search
* example: `find . -maxdepth 1 -name 'file1'` will search in the current directory for the file named `file1`


* The option `-size` allows to search for files with a specific size
* example: `find . -size +14k` will get the files greater than 14 kilobytes you


* There is also `a`, `c`, and `m` combined with `min` or `time` will help you to specify a search criteria `a` for `access`, `c` for `change`, and `m` for `modified`
* example: `find . -cmin -20` will get you all files that changed during the last 20 minutes


* Learn more about find from this [link](http://www.binarytides.com/linux-find-command-examples/)