# Getting Started

Never developed on your machine before? No problem! Start here to get your computer set up. 

This may seem like a lot, but all the steps are pretty straightforward. Feel free to ask for help!


## Step 1: Create a GitHub Account

If you don't already have one, sign up for an account [here](https://github.com/join)


## Step 2: Install Git

Type this into your terminal: `git --version`. If that prints our a version number, skip to step 3. If not, follow [this guide](https://www.atlassian.com/git/tutorials/install-git/) to get git set up. If you're on a Mac, I recommend following the Homebrew installation instructions.


## Step 3: Install Sublime Text

Sublime Text is a great, easy to use text editor. Download it [here](https://www.sublimetext.com/3).


## Step 4: Setup Sublime command line tool

It's going to be a lot easier to open files directly from the command line (rather than opening them with the file finder you're used to). To set this up, just paste this into your terminal and hit enter: 

`ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/subl`

Now, if you type `subl` before a file path, your computer will open the file with Sublime. This will be especially useful when you want to open a whole folder worth of files. To open the current folder in Sublime, type `subl .`


## Step 5: Set Sublime as your default editor

Now that you can open Sublime from the terminal, type this: 
`subl ~/.bash_profile`

This will open up a set of instructions that, among other things, can tell your terminal what program to use to open files. We're going to tell it to open files with Sublime by default. Paste this into the file, save, and exit: 

`which -s subl && export EDITOR="subl --wait"`

Now restart your terminal, and you should be set up to edit files with Sublime!


## Step 6: Install XCode command line tools 
Depending on the project you pick, you may not need to install this. It is a very useful tool that a lot of other libraries need, so it's not a bad idea to install it if it's not already on your machine.

First check if you already have it. Type `xcode-select -p`. If this prints out a file path, you're good to go. Otherwise, type:

`xcode-select --install`

If you see anything confusing, check out this article, which lays out the installation process pretty well: http://railsapps.github.io/xcode-command-line-tools.html

