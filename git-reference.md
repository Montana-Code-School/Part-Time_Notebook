# Git Reference

---
## Table of Contents
### Terms

[Git](#term-git)

[Repository](#term-repo)

[Pull](#term-pull)

[Add](#term-add)

[Commit](#term-commit)

[Push](#term-push)

[Forking](#term-fork)

[Branches](#term-branch)

### Walkthrough

[How do I install Git?]()

[How do I clone a repository?]()

[How do I fork a repository?]()

---

## Terms

<a name="term-git"></a>
### Git

**Git** is a *version control system*. Git allows you to track and manage changes made to a file, which also enables team members to work on the same files without conflicts.

In a development team, you will want to edit the same file as another teammate, and you might end up making changes at the same time. Git allows you to reconcile the differences between your changes, and meticulously log what changes were made, and when.

Finally, you can use Git to retrieve older versions of your file. Say you made a great improvement a month ago, but something has stopped working since then. You can checkout that file from a month ago, continue from there, all while keeping your current progress safe.

<a name="term-repo"></a>
### Repository

**In Short: A repository is the collection of files**

A repository exists alongside your project, and it is a collection of files that represent the history of all changes you've made.

The repository on Github is known as a *remote repository*. The repository on your own computer is known as the *local repository*.

<a name="term-pull"></a>
### Pull

**In Short: Pulling updates your local files**

**Pulling** in Git refers to the process of updating your *local repository* with any changes that have been stored in the *remote repository*. If another team member has changed a file and properly **pushed** it to Github, you will then **pull** those changes to your computer. You will do this using the `git pull` command.

(Make sure you are on the project root directory!)

```
austin@Austins-MacBook-Pro Part-Time_Notebook (master)*$ git pull
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 3 (delta 1), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/Montana-Code-School/Part-Time_Notebook
   d9d07de..f6d3cdc  master     -> origin/master
Updating d9d07de..f6d3cdc
Fast-forward
 README.md | 4 ++++
 1 file changed, 4 insertions(+)
```

<a name="term-add"></a>
### Add
**In Short: You can use add to finalize your changes, before committing and pushing them to Github**


<a name="term-commit"></a>
### Commit

<a name="term-push"></a>
### Push

**In Short: Push will update the files on Github's servers.**

When you have made changes on your *local repository*, you will want first **add** those files to staging, **commit** them, then **push** those changes to Github (the *remote repository*).



<a name="term-fork"></a>  
### Fork

Forking a repository means copying the repository and making your own changes to it from your account. It won't affect any of the code from the original repository, but will allow you to experiment and make your own customized version of it.

Once you make the changes that you need to make, you can then submit a *pull request*. A pull request will notify the owner of the repository of your changes, and will give them the opportunity to *pull* in what they think is appropriate.

<a name="term-branch"></a>
### Branch

---

## Walkthroughs

<a name="walk-install"></a>
### How do I install a Git?

<a name="walk-repo"></a>
### How do I clone a repository?

<a name="walk-fork"></a>
### How do I fork a repository?
