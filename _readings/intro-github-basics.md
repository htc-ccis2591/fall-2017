---
title: "GitHub Basics"
summary: "An introduction to file & version management using git on GitHub."
labels:
 - GitHub
 - git
---
# {{ page.title }}
This is an introduction to the Git & GitHub process you will use for your homework.  These steps and commands are also repeated in the follow-up experience
[GitHub: HTML Hello World]({{ "/experiences/intro-hello-world.html" | prepend:site.baseurl }})

## Prerequisites
Make sure that you have completed the following prerequisites before beginning:

- [Shell Basics]({{ "/readings/intro-shell-basics.html" | prepend:site.baseurl }})
- [Install Git]({{ "/experiences/intro-install-git.html" | prepend:site.baseurl }})

## Introduction
Throughout this course, we will be using Git and [GitHub](http://github.com/) to manage our projects. Git is an popular open source version control system, originally developed by Linus Torvalds (the creator of the Linux kernel). A large number of software projects, both open source and commercial, rely on Git for version control.

[GitHub](http://github.com/) allows us to have a centralized location to store and manage the git repositories.  While git can version files locally (on your computer), it is less risky to have copies of those versioned files in another location in case something happens to the files on your computer.  Since the repositories on GitHub are public, it is a great source for developers to show off their portfolio and to share your work with others.

Understanding how to work with Git (the underlying version control system behind GitHub) and [GitHub](http://github.com/) are both very important first steps in this course.

{% include youtube-16x9.html  id="gaSMO6MGKjs" %}


### Get a GitHub Account
Get yourself setup with a GitHub account.  I recommend that you add your name to the account profile so that others can easily search for and find your account and repositories. Please use something readable. __DO NOT__ use your school id or your Star ID.

If you associate your student email with GitHub, you can later request a free Personal account upgrade through the GitHub [Student Developer Pack](https://education.github.com/pack).  If you don't have access to your student mail right now, that's OK. Use an email you can access when you sign up.  You can always come back and change it or add an additional email later.


## The Git Command
The `git` command is one command with many varieties.  It can be used to do many different things, as if it were multiple commands. To you it is basically a series of different commands that all use git.  However to the OS it is one command to run `git` and then the OS stops caring, allowing `git` to decide what to do after that.


## Configure Git
Before you dive in, you'll want to configure git with your GitHub user information.  This is done using the `git config` command.

In the commands below, fill in your GitHub name in place of the `<user_name>` and the email used with your GitHub account in place of `<user_email>`.  The email address is what will tie your activity to your account.  **Make sure that you are using the same email used to sign up for GitHub and check carefully for typos.**


### Personal (Home) Computer
Use this on your home computer where you are the *only* GitHub user.  

{% highlight bash %}
$ git config --global user.name <user_name>
$ git config --global user.email <user_email>
{% endhighlight %}

### Public (Shared) Computer
Use this on a public a computer such as those in classrooms on campus, in the computer lab, or in the LRC.  This configuration is applied only to the current git repository directory, instead of the entire computer.  It must be repeated for each repository you clone or create.  

{% highlight bash %}
$ git config user.name "User Name"
$ git config user.email "user@email"
{% endhighlight %}

When you are done working on the public computer, you should make sure that you:

1. Have all changes pushed to GitHub.  Verify this using the web browser.
2. __Log out__ of GitHub so no one else can access your account.
2. Delete the local repository directory from the computer.  

If you do not delete files from a public computer, you risk someone else accessing your account and potentially stealing or removing your work. You wouldn't leave yourself logged into your bank account or email on a public computer, and likewise you shouldn't do the equivalent with GitHub. Your hard work is valuable too!

Since you will need to repeat the public config each time you use a public computer, I recommend saving a copy of this customized `git config` (with your user information) as a Gist on your GitHub account so that it is easily available for you to use on any public computer.

## Starting an Assignment

### Accept assignment
Most assignments will begin with a starter repository that you will accept using by clicking a link in the assignment instructions on the course web site.  The link will take you to a web page that prompts you to accept the assignment.  You must click the button to accept. This triggers GitHub to create a personal, private copy of the assignment repository and its files just for you (and the instructor) to see.

### Get the starter code
The personal copy of the starter code repository initially exists only on GitHub.  You'll need to *clone* the repository to your computer, so that you can make changes to the files. To do this, you use the `git clone` command followed by the URL for the repository.

{% highlight bash %}
$ git clone <repository-url>
{% endhighlight %}

{%  include youtube-16x9.html  id="iFP_Rfuc8wU" %}

Once you have cloned the code to your computer, it is important that you use the `cd` command to go into the repository directory before attempting to use the git commands for checking status or versioning files.

## Check Status
The `git status` command will give you the current status of your local repository. It will show you if you have changes that are untracked (not added), changes added and ready for commit, and how different your local repository is from the remote repository that you cloned from.

For example:
{% highlight bash %}
$ git status
{% endhighlight %}

## Version files
Versioning files is a two-step process.  First you must *stage* the changes, then you *commit* or version those changes that were staged.  This means that you can selectively choose which files to version, instead of versioning all files in your repository.

### Stage Changes
To stage your changes so that git knows the files are ready to be versioned, use the `git add` command.  Git does not just version all of the files in your repository.  It will only track and version files you specifically *add* to staging.  

To stage an individual file or directory:
{% highlight bash %}
$ git add <path>
{% endhighlight %}

To stage all changes in the current directory:
{% highlight bash %}
$ git add .
{% endhighlight %}

### Version Changes
When all your files are staged, then you do a *commit*.  This marks them with a version stamp inside your local repository.  It's a good habit to commit code locally often. You must include a message with your commit.  This should be a specific note on what you've changed in that commit.  This gives you a point to go back to if you need or want to undo something.

{% highlight bash %}
$ git commit -m "Some message in quotes."
{% endhighlight %}

The message should be in quotes so that you can use spaces in the commit message.  Make sure that you end the quote or the command will stay open and nothing will happen.

## Push files to GitHub
When you're done with a chunk of work, or just want to save it in the cloud for backup, you *push* your changes up to GitHub. To submit your completed assignments, you will need that work to be on GitHub in order to create the pull-request used for grading.

{% highlight bash %}
$ git push
{% endhighlight %}

{%  include youtube-16x9.html  id="EeW6mf5ZUZQ" %}


## Publish to the web
Once your changes are on GitHub, you can create a pull-request to move the changes from the __dev__ branch to the __gh-pages__ branch. After creating the pull-request and reviewing the changes, you should merge the changes.  You should be able to click the button to do this automatically if you are following this workflow process correctly.

{% include alert.html type="warning"
    content="You can push any changes up to the dev branch to ensure they are backed up and not lost. However because this pull-request pushes the files to the gh-pages branch which publishes the files to the web, you should only merge changes after you have tested them successfully on your computer and they are ready to go live on the web."
%}

## Test and validate
Before creating the final pull-request for grading, you need to test and validate your website to make sure that everything is correct. You can get the URL from the GitHub repository page.  Click on the Settings tab and scroll down. You should see highlighted in green the URL where your page is published.

When you click the URL, you should see the home page for your site. If the page is not coming up, check your email to see if there was an error in publishing.  If you continue to have problems, email the instructor for assistance.  Note that it sometimes takes a while before changes to the site are published.  It is usually immediate, but on occasion I have seen it take hours.

Make sure to test *AND* validate all pages of your site before submitting the work for grading.


## Submit for grading
When you have finished your final testing and are ready for your work to be graded, create a pull-request between the __gh-pages__ branch and the __grading__ branch.  This is the last - but most important - step, the one that turns in your assignment.

__DO NOT MERGE__ this pull request. For the work to be graded, the pull-request must be left open.
