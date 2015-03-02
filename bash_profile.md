---
layout: page
title : Bash Customization
---

Customizing your shell terminal
===============================

Code to customize your terminal lives in the file `.bash_profile` in your home folder. This is a plain text file that you can add to using any text editor.

Any commands that you can run interactively at the terminal command prompt can be put in here to be executed each time the terminal is opened.

Aliases
-------

A Bash alias is essentially nothing more than a shortcut, a means of avoiding typing a long command sequence, or it can save us from having to remember it.

We can come up with a new name for a command 

`alias fn='find . -iname'`

which we can then run on the command line using the shortcut, e.g.:

`$ fn "mouse*.raw"`

which would search the file system, starting in the current folder for all files that begin with "mouse" and have a ".raw" extention

we can also re-assign commands so that they have certain options by default

`alias ls='ls --color'`

The prompt string
--------------------

We can change the text and color of the prompt by redefining the PS1 variable. We can include plain strings, or use [special characters](http://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html) and [color](http://www.cyberciti.biz/faq/bash-shell-change-the-color-of-my-shell-prompt-under-linux-or-unix/).

This, for example, will work, if not particularly useful:

`PS1="Hi Amy! :"`

Here is what I have mine set to, for example:

`PS1="\e[0;32m\t \w\$ \e[m"`

Notice that Bash prompts usually end in a `$`, but this is by convention only. Here is an example of a longer one that uses multiple colors:

`PS1="\e[0;32m\u \w \e[m\e[0;35m \t \e[m\$\n"`

Updating your path
------------------

To see what is currently on your path type

`$ echo $PATH`

to add to your path use:

`PATH="$PATH:/path/to/new/folder"`