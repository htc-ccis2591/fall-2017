---
title: "Shell Basics"
summary: "An introduction to using the shell on Windows and Mac."
---

# Shell Basics
When I refer to "the shell", I am referring to the command line in an operating system neutral way. If you are on a Mac, this means Terminal. If you are on Windows, this means PowerShell (or for specifically working with git you can use Git Bash).

There are only four main commands that you'll need to know for this course:

- pwd
- ls
- cd
- git

The last command, git will be covered separately as it's a little more complex.

## Don't type the $
When I include shell commands in the notes, the lines will always begin with a $ (dollar sign). That indicates the prompt or the start of the shell command line. The exact display of the *prompt* will look different based on what type of computer you are using, so we use the $ to represent a generic prompt.  _When entering commands do not type in the $; only type in the text that follows it._

Having the $ there to indicate the prompt is important. It allows us to distinguish input and output in the examples. Lines that begin with the $ show the commands that you would type in.  Any lines without the $ at the beginning of the line, will show you sample output from entering a command. Note that many commands do not give you output when successful.

## Present Working Directory (pwd)
The first command we will learn is the `pwd` command. I try to remember this as an acronym for "present working directory". This tells you which directory you are currently working in for that shell window. Basically, this tells you where you are located within your computer's file system tree.

Here's an example:

<div style="padding:10px">
<div class="row">
<div class="col-xs-12 col-md-6">
  {% highlight bash %}
  $ pwd
  /Users/marymosman/Development/html/students
  {% endhighlight %}
</div>
</div>
</div>

Remember, when you try out this command, only type `pwd` into your shell window, do not type the $, then hit enter. It will output your current working directory on the next line, which will be different from the example shown.  It will then give you a prompt again.   

This is what it actually looks like on my computer.  I'm running on a Mac, so this is the Terminal.
{% include img-medium.html url="/assets/images/intro-shell-basics/terminal-pwd-cmd.png"
    alt="Terminal on a Mac showing the results of the pwd command."
%}

## List Directory Contents
The `ls`, or list, command will list all of the files and directories inside the current working directory.

{% highlight bash %}
$ ls
file1        file2        directory1        directory2
directory3   file4        file5
{% endhighlight %}

{% include img-medium.html url="/assets/images/intro-shell-basics/terminal-ls-cmd.png"
    alt="Terminal showing the results of the ls command"
%}


## Change Directory
The `cd`, or change directory, command will change your working directory. When you enter the command, you type the directory to change to after the `cd`.  

So if we want to go into the _data directory, we would enter:

{% highlight bash %}
$ cd _data
{% endhighlight %}

This command does not produce any output unless there is an error.  Make sure to pay attention to each commands output and watch for any error messages.

{% include img-medium.html url="/assets/images/intro-shell-basics/terminal-cd-cmd.png"
    alt="Terminal showing cd command"
%}

Again, notice there is no output.  

### Go back, or go to parent directory
To go up a directory you use two dots (or periods) after the `cd`.  

{% highlight bash %}
$ cd ..
{% endhighlight %}

Again there is no output, but you can use the `pwd` command to see that the working directory has changed.


{% include img-medium.html url="/assets/images/intro-shell-basics/terminal-cd2-cmd.png"
    alt="Terminal showing cd .. command"
%}


## Other Resources
While these commands (plus the git commands you will learn later) are enough to get by for this course, shell commands are important tools for IT Professionals. This article from LifeHacker offers a quick overview of why you should learn to use the command line, and how to do it:  [Master the Command Line This Weekend](http://lifehacker.com/5990668/master-the-command-line-this-weekend).

Codecademy also has an online course to [Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line).  Unit 1 and Unit 2 provide sufficient knowledge for this course, and the last time I checked you were able to work through those with a free account.

Neither of these additional resources are required for this course, but being comfortable working in the shell will be a useful skill to have long-term.
