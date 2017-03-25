# Command Line Reference  

---

## Table of Contents

[What is the command line?](#what-is-commandline)

[How do I find it?](#how-to-find)

[Common Commands](#common-commands)

<a name="what-is-commandline"></a>
### What is command line?

The command line is simply a means for using lines of text to communicate with programs on your computer. If you haven't used it much yet, you will become very familiar with it as a programmer.

<a name="how-to-find"></a>
### How do I find it?

For everyone on a Mac, it is called *Terminal*, and you can find this in your applications, or by pressing the `command + space` buttons to open up Spotlight Search, then type *Terminal*.

For those of you using Ubuntu, you can press `Ctrl + Alt + T`, or navigate to it using *Dash Home*, which is similar to Spotlight Search on Mac.

### A few things first

When working in the terminal, you will immediately see something like this:

```
austin@Austins-MacBook-Pro ~ $
```

First, you see your user's name. Then you see the name of the computer that is being used. Followed by this, there is a `~`, which refers to *the current directory*. A tilde (~) refers to the **Home** directory, which is likely the folder that belongs to your user. As you move to different folders, that tilde will change to reflect the directory that you are currently in.

#### File Paths

You will see two types of file paths, *absolute paths and relative paths.*

An *absolute path* refers to the full path, from the root of the file system:

```
/Users/austin/Movies/Vertigo - Alfred Hitchcock.mp4
```

A *relative path* refers to where a file is *relative* to your current directory.

If you are looking for a file in your current folder, you will use `./folder-name`, but if you want to get a file that is *next* to your current folder, you can move one level up with `../my-other-folder`. It's not uncommon to see something like `../../../../some-folder`.

---

<a name="common-commands"></a>
### Common Commands

#### sudo

**sudo** is a command that allows you to override any file permissions and perform actions as the superuser.

There is a reason some commands require sudo, at times you are performing operations that can be harmful. Don't use sudo without being sure about what you are doing.

#### man

First of all, man is a useful command to display manual pages. If you don't remember how a command works, just type `man {command}`.

```
man ls

LS(1)                     BSD General Commands Manual                    LS(1)

NAME
     ls -- list directory contents

SYNOPSIS
     ls [-ABCFGHLOPRSTUW@abcdefghiklmnopqrstuwx1] [file ...]

...
```

---

#### ls
Use ls to list all files and folders in your current directory.

```
austin@Austins-MacBook-Pro / $ ls
Applications			Users				data			installer.failurerequests	 tmp
Library				    Volumes			dev				net				                 usr
Network				    bin				  etc				private				             var
System				    cores				home			sbin
```
Note: You can also view hidden files with the option, -a.

---

#### cd
cd is an essential command for the terminal. cd will allow you to *change directory*, allowing you to move from one folder to another.

```
austin@Austins-MacBook-Pro ~ $ ls
Applications					 Dropbox							Public
Creative Cloud Files	 Library							Sites
Desktop							   Movies							  
Documents						   Music							
Downloads						   Pictures
austin@Austins-MacBook-Pro ~ $ cd Movies/
austin@Austins-MacBook-Pro Movies $ ls
Vertigo - Alfred Hitchcock.mp4
```
---
#### mkdir
mkdir is the command to *make a new directory*. Essentially it is your New Folder method in command line.

```
austin@Austins-MacBook-Pro Desktop $ ls

austin@Austins-MacBook-Pro Desktop $ mkdir my-new-folder
austin@Austins-MacBook-Pro Desktop $ ls
my-new-folder
```
---
#### mv

mv is the *move* command, allowing you to move a file or directory to another location. Below, I am moving `new_file` from `my-new-folder` to `Desktop`.

```
austin@Austins-MacBook-Pro my-new-folder $ ls
new_file
austin@Austins-MacBook-Pro my-new-folder $ mv new_file ../new_file
austin@Austins-MacBook-Pro my-new-folder $ cd ../
austin@Austins-MacBook-Pro Desktop $ ls
my-new-folder	new_file
austin@Austins-MacBook-Pro Desktop $
```
---

#### cp
cp is the *copy* command, and works very similarly to the mv command.

---

#### rm

rm is the *remove* command, allow you to *delete* files from the command line.

**WARNING: Files deleted with rm will not go to the trash! They will be gone!**

```
austin@Austins-MacBook-Pro Desktop $ ls
new_file
austin@Austins-MacBook-Pro Desktop $ rm new_file
austin@Austins-MacBook-Pro Desktop $ ls
austin@Austins-MacBook-Pro Desktop $
```

To remove a directory, you will need to use the -r option, which will remove all files and folders within that directory as well, or use `rmdir` instead

```
austin@Austins-MacBook-Pro ~ $ ls
my-new-folder
austin@Austins-MacBook-Pro ~ $ rm my-new-folder/
rm: my-new-folder/: is a directory
austin@Austins-MacBook-Pro ~ $ rm -r my-new-folder/
austin@Austins-MacBook-Pro ~ $ ls
```

---
