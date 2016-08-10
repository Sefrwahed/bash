---
layout: main
title: Analyzing Text Files
---

# Analyzing Text Files

## cat or tac

### `cat`

* Shows content of a specific files
* Example: `cat file`

> cat is short for **concatenate**, WHY?

* You can concatenate multiple files
* example: `cat file1 file2`

### `tac`

* Just like `cat` but shows a reversed content

## head and tail commands

### `head`

* Displays **top n** lines of a file
* example: `head -n 10 file` shows first 10 lines of file

### `tail`

* Displays **bottom n** lines of a file
* example: `tail -n 10 file` shows last 10 lines of file
* A fantastic advantage of `tail` is the **follow**
* example: `tail -f file` will show the newly added lines in the file

## more or less

### `more`

* Lets you scroll forward **only** in a file with a percentage
* example: `more big_file`

### `less`

* Lets you scroll forward and backward in a file
* example: `more big_file`
* You also able to a line number with `#G` where **#** is line number
* Also you can search the file with `/word`, replace word with whatever you search for

## cut and sort

### `cut`

* Lets you extract some info from files using a delimiter and field number
* example: let's try this `cut -f 1,3 -d ','` on a **csv** file

### `sort`

* Lets you sort file content with specific order
* example: let's try `sort` and `sort -r` on our **csv** file
* example: let's try `sort -t ',' -k 3`  on our **csv** file
* We also can use `-n` if we are sorting numbers
* example: difference between `sort -t ',' -k 3` and `sort -t ',' -n -k 3` on our **csv** file