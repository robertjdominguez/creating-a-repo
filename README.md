# Basics of Git / GitHub

This resource is the first "do something" activity that's a part of our learning path. Now that you have a bit of knowledge as to what Git / GitHub are and their differences, we're going to put your knolwedge / skills into action :tada:

## Overview

**Your goal: create a repository locally on your device.**

To achieve this, follow these steps:

### 1. Download and install Git for Windows

[This link](https://git-scm.com/download/win) should start your download immediately. Follow the installation instructions. While it's important that Git is being installed, it's equally important that you're getting a new command-line tool called Git Bash. This enhances your Windows machine's ability to use great, quick 'shortcuts' / commands (that are commonplace on macOS and Linux-based machines).

### 2. Open Git Bash - you can find this in your programs after completing the above step

Before we go on, yes: there are graphical clients where you can point-and-click your way through Git operations. However, we're going to use Git Bash and the command-line interface to complete this 'course'. Why? It's all about the basics...writing the commands will help you to understand what's _actually_ happening. These details can get lost when using a GUI. However, after we're all done, if you wish to use a graphical Git client, go for it :rocket:


### 3. Create a new `Learning` directory

We want to keep things tidy. Remember, `repository === directory === folder`. Slight exaggeration, but an effective mental model. 

To create your new directory, it's helpful to have a 'sandbox' somewhere on your machine. Essentially, a folder called `Projects` or `Learning`. You can create this first if you wish:

```bash
# mkdir = make directory
# mkdir <directory_name>
> mkdir Learning
```
Now that you've created that directory, let's move into it:

```bash
# cd = change directory
# cd <path>
> cd Learning
```

### 4. Create a subdirectory for this first assignment

Now that we're in `Learning` and you've satisfied my OCD, let's create a new directory for this assignment:

```bash
> mkdir git-assignment-1
```

Then, let's move into it:

```bash
> cd git-assignment-1
```

### 5. Initialize a Git repository

We have a directory, but there's nothing special about it...yet. However, running the following command will turn this directory into a Git repository:

```bash
# 'git' is the program and 'init' is the command to initalize / create -- this pattern / structure is commonplace with command-line tools
> git init
```

Congrats! You have a repository! But...so what? Let's do a couple of things to see why this is a big deal.

### 6. Create a new file

We're not going to write any code during this set of workshops. Everything will be using a format called markdown (`md`) that you've seen us discuss / use in Docs. It allows for rich text by using a minimalistic syntax (language structure).

```bash
# touch = create
# touch <file_name.extension>
> touch readme.md
```

We can see the new file has been created one of two ways. First, let's keep things in Git Bash:

```bash
# ls = list; no argument needed for current directory
> ls
```

You should see a list returning the contents of your current directory...hopefully it's just `readme.md` :sweat_smile:

Alternatively, you could open up your Windows File Explorer and navigate to this directory. Do that too just to see we're not making things up...your file is actually there! **You** did it you :nerd_face:

### 7. Edit the `readme.md` file

For now, we're going to keep things in the command line. We can use the following command to write a string (characters that are parsed as text) to our `readme.md`:

```bash
# echo = repeating of a value, but we can write to an already-existent file using >>
# echo <value-surrounded-by-quotation-marks> >> <file>
> echo "Hello, World!" >> readme.md
```

If you look inside `readme.md`, you should see your new text :tada:

### 8. Let's recap

So far, what have we done? Well...

- We've created a new directory
- We've turned it into a Git repository
- We've created a new file
- We've edited that file's contents

But...what's the point of Git? Let's run the following command and see what comes up:

```bash
> git status
```

You should see some information about tracked vs. untracked files. This is Git observing and keeping track of what changes you make! Let's creat a commit - or a snapshot - that allows us to mark the status of our project at this point in time:

```bash
# add will...add
# git add <file-to-add>
> git add .
```

Using the period says, "Take everything here that's been updated / created /deleted / modified." Which, for us, is only one file: `readme.md`.

Now, let's actually create the commit:

```bash
# commit is the command for creating the commit which contains all the relevant files; -m is a flag that allows you to write a message
# git commit -m <message-text>
> git commit -m "create readme.md"
```

### Step 9. Let's check the log

With the `git log` command, we can see the commit history of the repository. This allows us to go through a 'timeline' of all the changes to a repository and different snapshots through the life of a project:

```bash
# log = show me the commits / commit history
> git log 
```

You can press `q` to quit and come back to your Git Bash shell.

## Recap

So...that took longer to write than I thought. Hopefully, even though there's many steps here, this is something you can play around with. Emphasis on **play**! Take this process, repeat it. Create new directories, search when you get stuck, and shout at me with questions! Reading and watching videos is one thing...but there's no replacement for actually getting your hands dirty...especially since you won't break anything :wink:
