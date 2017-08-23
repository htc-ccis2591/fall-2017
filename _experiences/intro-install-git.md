---
title: "Install Git"
summary: "Install and configure git on a Windows or Apple computer."
---

# {{ page.title }}
The install process for git is different based on the type of computer you are using.  Install information is provided here for Windows & Mac OS.  If you are using Linux, it is likely that you already have git, and if not I assume you can use the package manager to install it.

## Windows Users
If you are a Windows user, typically you will use PowerShell as your command shell.  However, Windows PowerShell does not include git by default.  You will need to download and install git from the web. You can get it from the [Git-SCM Downloads](https://git-scm.com/download/win).

I recommend that you keep the default install settings suggested by the installer, specifically:
<div class="row">
<div class="col-md-6">
<img class="img-responsive" src="{{ "/assets/images/intro-install-git/git-install-opt1.png" | prepend:site.baseurl }}" alt="Screenshot of install options">
</div><div class="col-md-6">
<img class="img-responsive" src="{{ "/assets/images/intro-install-git/git-install-opt2.png" | prepend:site.baseurl }}" alt="Screenshot of install options">
</div>
</div>

<br>
These settings will install a few different options for working with Git on a Windows computer.  However, I recommend using __GitBash__ as it will be closest to what you see in my examples. If you use other options, such as the Windows Command Prompt, some commands (such as `ls`) used in my examples may not work correctly.


## Mac Users
If you are using a Mac, open up a [Terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) window and type git.  You may find that Git is already installed, or if not that it will prompt you to install the XCode Command Line Developer Tools.  If it does not, you likely have an older version of the Mac OS and should download and install the those XCode tools from the [Apple Developer Site](https://developer.apple.com/downloads/index.action).  You can also install the full XCode suite from the Apple App Store, but this will take additional space.  


## Questions or Problems?
This is a quick overview that assumes you have some familiarity with downloading and installing software for your system.  If you need additional help or have questions or problems with the install process, please email as soon as possible so that we can work together to get any issues resolved. In your email, please include information on the operating system on your computer and any details (screenshots if possible) on the problems or questions you have.  The more detailed the email, the more likely I will be able to give you specific and meaningful help right away.
