# Git

## Why Git?

Consider a scenario where you are working on a project
(not necessarily an [APOGEE](http://bits-apogee.org) project.
By project I mean any big collection of code written to do something useful)
with a team of 2 others.
You all are working on the same code.
You write a small piece of code first and now
you want to share your code with others so that they can build upon it.
How will you do it?

Here are some options:

1.  You can email your code to others.
2.  You can use a shared folder on Dropbox (or a similar site).

Both these approaches are prone to errors and are not scalable.
In Dropbox, you might run into sync conflicts.

Think of a massive project like Firefox.
It has thousands of people working on the same code and there are around 75 code submissions each day.
The above techniques will clearly not work there.

People have come up with a smart solution for managing source code.
It is called a **Version Control System (VCS)**.
Git is the most popular VCS.

In BITS-ACM, most (if not all) second and third yearites
will be using Git for managing code for events this APOGEE.
If you want to contribute, you'll have to learn Git.
You must know Git if you want to participate in
[Google Summer of Code](https://developers.google.com/open-source/gsoc/).

## How to learn Git

[Git Tower's Tutorial](http://www.git-tower.com/learn/ebook/command-line/introduction) is pretty good.
Read parts 1, 2 and 3 completely.
Also read the [best practices](http://www.git-tower.com/learn/git/ebook/command-line/appendix/best-practices#start).
If you want to learn more, you can look at the [Pro Git book](https://git-scm.com/book/en/v2).

You might not understand how important Git is, but believe me,
you'll surely benefit by learning it and you will gradually realize how useful it is.
So learn it well.
Use Git for any project you are working on.

Unless you master the command-line interface of Git, you must not move to any GUI Git client.
You might not even need a GUI client after learning that much.

To collaborate, you must host your git repository online so that others can access it.
There are many free git repository hosting services available.
[Github](https://github.com) and [Bitbucket](https://bitbucket.org) are the most popular ones.

## Installing Git

*  Windows users: [https://git-scm.com/download/win](https://git-scm.com/download/win)
*  Linux users: `sudo apt-get install git`

## Advice for Linux users

In [Git Tower's book's part 1.3 (Getting Ready)](http://www.git-tower.com/learn/git/ebook/command-line/basics/getting-ready#start),
the authors have a list of commands to configure git.
Add this command to that list:

    git config --global core.pager 'less -+FSX'

## General advice

Always run `git diff --check` before staging changes.
This will make sure your files follow conventions for whitespace.
