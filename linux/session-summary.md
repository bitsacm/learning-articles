---
parent: linux
label: session-summary
title: Linux session summary
bigtitle: Summary of the introductory session on Linux
---

# {{page.bigtitle}}

by [Eklavya Sharma](https://github.com/sharmaeklavya2)

The first session on introduction to Linux was held on 12 October 2015, Monday at 5:30 pm.
A lot of first yearites and a few 2nd yearites turned up for the event.
The event focused on teaching the fundamentals of Linux.
Students were also introduced to the command line interface.

I have made a structured summary of what I taught.
I hope this helps.

Everyone, start using Linux.
You might not like it initially.
Resist the temptation to use Windows.
Gradually you will start liking Linux.
And hopefully it will become the OS of your choice.

Linux is very developer-friendly (I'm not saying it's bad for non-developers).
To experience the power of Linux, start using Linux for
whatever you are learning, be it C/C++, Java, Python, web-dev or anything else.

## Topics discussed:
1.  OS
    * What is an OS?
        (practical definition - platform to run programs,
        actual definition - An operating system (OS) is system software that manages
        computer hardware and software resources and provides common services for computer programs)
    * Interfaces (GUI vs CLI) (kernel and interface make up an OS)
    * Advantages of CLI - repeatability, backup, remote access
2. Terminal and terminal emulator
    * What is a prompt?
    * Difference between terminal (emulator) and shell
3. Paths
    * Tree structure
    * Multiple trees by drives letters in windows. Single root directory in Linux
    * Paths: absolute, relative, `..`, `~`
4. Commands
    * Short note on shell builtins
    * Command line arguments
    * basics of IO redirection
5. Users and permissions
    * Users and groups
    * Owner and group of a file
    * Permissions of a file (3 types of actions, 3 types of users, so 9 boolean fields)
    * Superuser

## Important commands discussed during the session:
* `cd`   - change directory - changes the current working directory (`chdir` in windows)
* `pwd`  - print working directory
* `ls`   - list things in a directory (`dir` in windows)
* `less` - show the contents of a file in a pager
* `cat`  - output the contents of a file
* `echo` - output the command line
* `help` - help on shell builtins
* `man`  - manual page - help on external commands

Keep practicing these commands regularly.
These are especially important if you are interested in shell scripting.

## Where to learn more from:
I learned a major part of what I know from <a href="http://linuxcommand.org/lc3_learning_the_shell.php">`http://linuxcommand.org/lc3_learning_the_shell.php`</a>

Some people have also suggested the [EdX course](https://www.edx.org/course/introduction-linux-linuxfoundationx-lfs101x-2).

## Things I could not teach or I forgot to teach:
* `PATH` environment variable
* tty
* '.' in paths
* running executables in cwd
* vim
* package-management
* Ctrl+C
* Ctrl+D (EOF)
