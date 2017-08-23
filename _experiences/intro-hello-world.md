---
title: "GitHub: JS Hello World"
summary: "Practice using the shell, git and GitHub to get, create, update and manage files."
---

# {{ page.title }}
{{page.summary}}


## Prerequisites
Make sure that you have completed the following prerequisites before beginning:

- [Install, Configure, and Use Brackets]({{ "/experiences/intro-brackets.html" | prepend:site.baseurl }})  
- [Install Git]({{ "/experiences/intro-install-git.html" | prepend:site.baseurl }})
- [Shell Basics]( {{ "/readings/intro-shell-basics.html" | prepend:site.baseurl }})
- [GitHub Basics]( {{ "/morea/intro-summer/read-github-basics.html" | prepend:site.baseurl }} )


## GitHub Assignment Workflow
To help you get started working with GitHub, we'll practice working through an assignment together.  In this assignment, we'll accept the GitHub assignment, then clone it to our local computer to complete. When we've completed the assignment, we'll version the files and push them to GitHub.  Then we'll create the pull request for grading.



### Accept the assignment
Your assignments from this class will be completed in personal, private repositories created specifically for you.  To create the repository, you will need to accept the assignment using the link provided in the instructions.  

Click the link below, then on the web page, click the green button to accept the assignment.

[GitHub Assignment: JS Hello World](https://classroom.github.com/a/y95UUco6)


### Get the local repository
Once you have created the additional branches, you will need to *clone* the repository in order to complete the assignment.  

The `git clone` command will create a local copy of your repository from GitHub. The GitHub repository, what you see when looking at the website, lives on their servers "in the cloud".  That is a remote repository.  To work on your files, you need a local repository; one that is on your computer.

{% highlight bash %}
$ git clone <url>
{% endhighlight %}


### Use Brackets to edit the website
Once you have the repository files, open the repository directory in Brackets using File -> Open Folder.  Create any new files required by the assignment, or edit the existing files as needed to complete the work.  Use the Live Preview feature to test your site locally, and use Brackets Beautify to clean up your code before turning it in.

For this assignment you'll need to create an index.html page, and a JS file. Let's call the JS file script.js.

#### HTML File
First, create the index.html file. can just start out by making an index.html file, and then copy and paste in the basic HTML template shown below:
{% gist mbMosman/5785c6e9534e956b79d7 basicHTML5.html %}

After pasting in the above HTML, edit it as follows:

1. Remove line 5 to delete the `<link>` tag, since we will not have a style sheet for this assignment.  (Feel free to add one if you like, but it isn't required.)
2. Update the title to "JS Hello World".
3. Delete the `<p>` tag so that the body is empty.
4. Add a `<script>` tag to write "Hello World" to the console.
5. Add a second `<script>` tag to run your script.js file. It is considered a best practice to put script tags that reference files at the end of the body.

#### JS File
Next, create your script.js file.  Add code to write "Hello World" to the DOM so that it shows up on the web page. 

### Test
Run your page through Brackets Live Preview feature.  You should see Hello World in two places: 1) on the page itself, and 2) in the console.

You'll need to open up the browser console to see the Hello World from the JS embedded in the HTML page. In Chrome, and most browsers, this is part of the Developer Tools.


### Version the modified files
Versioning the files requires using the `git add`, `git commit`, and `git push` commands.

First, select and stage the files using `git add`.  This marks them as ready for commit. These are tracked vs untracked files in git.  Untracked changes have not been staged and will not be part of a commit. You may see these called out by the `git status` command.

To add all changes, you can use this shortcut:
{% highlight bash %}
$ git add .
{% endhighlight %}

To add individual changes, you can use add plus the file name or directory to add:
{% highlight bash %}
$ git add <file-or-directory-name>
{% endhighlight %}

After staging the files, it is recommended you use `git status` to verify the outcome is correct. Your files should now indicate they are ready for commit.

The `git commit` command will save and version your changes to your local repository. You are required to enter a commit message, which should be in quotes.  The commit saves the time of the commit, all of the changes to the staged (added) files, as well as the message that you enter.  These changes are then ready to push to the remote repository.

{% highlight bash %}
$ git commit -m <message>
{% endhighlight %}

After committing the files, it is recommended that you again use `git status` to verify the outcome is correct.

Once the files have been committed, you may optionally *push* them up to GitHub.  You should do this when you have completed a chunk of work, or when you want to save it *in the cloud* to move changes between computers or for backup purposes.  

The `git push` command sends your local changes to the remote repository. If your local and remote branches match, you use the short form of the command:
{% highlight bash %}
$ git push
{% endhighlight %}

After pushing the files, it is recommended that you again use `git status` to verify the outcome and also check the GitHub website for the updates.


### Publish to the web
Once your changes are on GitHub, you can create a pull-request to move the changes from the __dev__ branch to the __gh-pages__ branch. After creating the pull-request and reviewing the changes, you should merge the changes.  You should be able to click the button to do this automatically if you are following this workflow process correctly.

{% include alert.html type="warning"
    content="You can push any changes up to the dev branch to ensure they are backed up and not lost. However because this pull-request pushes the files to the gh-pages branch which publishes the files to the web, you should only merge changes after you have tested them successfully on your computer and they are ready to go live on the web."
%}

### Test and validate
Before creating the pull-request for grading, you need to test and validate your website published from the gh-pages branch to make sure that everything is correct. You can get the URL from the GitHub repository page.  Click on the __Settings__ tab and scroll down. You should see highlighted in green the URL where your page is published.

When you click the URL, you should see the home page for your site. If the page is not coming up, check your email to see if there was an error in publishing.  If you continue to have problems, email the instructor for assistance.  Note that it sometimes takes a while before changes to the site are published.  It is usually immediate, but on occasion I have seen it take hours.

Make sure to test *AND* validate all pages of your site before submitting the work for grading.


### Submit for grading
When you have finished your final testing and are ready for your work to be graded, create a pull-request between the __gh-pages__ branch and the __grading__ branch.  This is the last - but most important - step, the one that turns in your assignment.

__DO NOT MERGE__ this pull request. For the work to be graded, the pull-request must be left open.  You should *NEVER* merge pull-requests to the __grading__ branch.

Make sure to take a screenshot of the open pull-request to put in the assignment box on D2L.  

You can take a screenshot on most windows computers by looking for the PrtSc or PrtScn button on your keyboard.  That will screenshot the entire desktop.  If you use Alt + PrtScn that will screenshot the active window.  This puts the screenshot in the clipboard.  You will need to paste this into a MS Word document to save and submit it.

On Mac, you can take a screenshot by using the command+shift+4 key combination.  This will allow you to select the area on the screen to screenshot.  If you hit the space key, it will change to highlight the active window for the screenshot.  Click the mouse to take the screenshot and it should save to your desktop.
