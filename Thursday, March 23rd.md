# Thursday, March 23rd

---
## Exercise for Command Line

### What is command line?

The command line is simply a means for using lines of text to communicate with programs on your computer. If you haven't used it much yet, you will become very familiar with it as a programmer.

### How can I get to it?

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

### Common Commands

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

## Exercise for Git

## What is Git?

We will need to begin using Git for our assignments. As you've seen in the pre-work, Git is a system for tracking changes to files, and helps teams work on those files at the same time.

Let's go ahead and dive into some exercises and figure out how we can submit our assignments.

1. [Go to our project repository.](https://github.com/Montana-Code-School/Simple-HTML-Site)
2. In the upper right, you want to click the button labeled "Fork".
3. Now, you can clone your new forked repository. Copy the line that appears after clicking "Clone or Download".
4. Open up your terminal, navigate to where you are keeping your projects, and enter `git clone URL`, with URL being what you copied from Github. This should look something like this:

```
austin@Austins-MacBook-Pro Class-Projects $ git clone https://github.com/aceslowman/Simple-HTML-Site.git
Cloning into 'Simple-HTML-Site'...
remote: Counting objects: 17, done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 17 (delta 1), reused 17 (delta 1), pack-reused 0
Unpacking objects: 100% (17/17), done.
austin@Austins-MacBook-Pro Class-Projects $
```

5. Now you can make any changes you want to this. I would recommend moving your project files into this repository, copying the contents of your HTML, CSS, JavaScript, and moving your images into place.

6. Once you are done with this, go to your terminal. Make sure you are in your project root directory. From there, you can type `git status`. You can see which files have been modified, added, or removed.

```
austin@Austins-MacBook-Pro Simple-HTML-Site (master)*$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   style.css

no changes added to commit (use "git add" and/or "git commit -a")
austin@Austins-MacBook-Pro Simple-HTML-Site (master)*$

```

7. Now, use `git add .` to stage all of your changes to be committed. You can also add individual files by using the filename instead of the `.`.

8. Now we need to commit our changes, and then push them to Github. You commit your staged changes using `git commit`, and can use this syntax to add your commit message in the same command: `git commit -m "Description of the changes that were made"`.

```
austin@Austins-MacBook-Pro Simple-HTML-Site (master)*$ git commit -m "Updated my stylesheet"
[master 4404c18] Updated my stylesheet
 1 file changed, 1 insertion(+), 1 deletion(-)
```

9. Now, push your commit to Github, using `git push`.

```
austin@Austins-MacBook-Pro Simple-HTML-Site (master)$ git push
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 309 bytes | 0 bytes/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/aceslowman/Simple-HTML-Site.git
   e7d5e5a..4404c18  master -> master
austin@Austins-MacBook-Pro Simple-HTML-Site (master)$
```

10. Now, once all changes are finished and you are ready to turn in your assignment, go to your forked repository and press "New Pull Request". You will then see a screen showing your changes, and once reviewing them, you can click "Create Pull Request".

11. Now I will receive a message indicating that a pull-request was submitted, and you are done!

---

### Forking

Forking a repository means copying the repository and making your own changes to it from your account. It won't affect any of the code from the original repository, but will allow you to experiment and make your own customized version of it.

Once you make the changes that you need to make, you can then submit a *pull request*. A pull request will notify the owner of the repository of your changes, and will give them the opportunity to *pull* in what they think is appropriate.
