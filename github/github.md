# GitHub



This page covers setting up [GitHub](https://github.com) and using it for your test repository.

GitHub is a tool used to store open-source code (such as test suites) and allow people to collaborate on it.

It's logical and powerful but not immediately intuitive, so this guide aims to make it easier.

In short, it helps you create a copy (branch) of existing code, make changes to it, commit (save) them, push them back to GitHub, get the changes reviewed via a pull request, then merge them into the main code.

Some terminology:
* **Git** is the core version control system that you access through your command prompt.
* **GitHub** is the website which shows everyone's code, and manages pull requests.
* **GitHub Desktop** is the (optional) desktop app that makes it easier to work with your project without using the command prompt.

## Setup

If you're new to GitHub then the [GitHub Hello World tutorial](https://guides.github.com/activities/hello-world/) is worth doing. The [Defra Digital Service Team guides](https://github.com/DEFRA/dst-guides/tree/master/github) also contain a lot of useful information.

You will need:

* An off-network Mac or PC
* On a Mac, it's worth installing [Homebrew](https://brew.sh/) first, to make it easier to install lots of other things.
* A [GitHub](https://github.com/) account that meets [Defra security requirements](https://github.com/DEFRA/dst-guides/tree/master/github)
* Access to push to your repository - contact an existing member of the team.
* A command line tool such as Terminal on Mac (built in) or [git bash](https://gitforwindows.org/) on Windows
* A text editor such as [Atom](https://atom.io/)
* A means to upload to GitHub. You can use the command line directly, or an app such as [GitHub Desktop](https://desktop.github.com/).

Once you have these, then:

* [Install and set up Git on your machine](https://www.atlassian.com/git/tutorials/install-git). Alternatively, there are some useful [Mac-specific setup instructions from Alan Cruikshanks](https://github.com/Cruikshanks/mac-setup/blob/master/git.md).
* Navigate to the root folder in your command line with `cd ~`
* Create and navigate to a projects folder: `mkdir projects` and `cd projects`
* Copy the latest code from the repository you're working with. For example, `git clone https://github.com/DEFRA/qa-test.git`
* Navigate to the prototype folder: `cd qa-test`

You should now be ready to start work on a repository.

## Some principles

* [We work in the open by default](https://www.gov.uk/service-manual/service-standard/point-12-make-new-source-code-open).
* However, do NOT publish usernames, user data, keys and passwords on GitHub. Speak to a colleague if unsure.
* Everyone makes mistakes, so always get a colleague to review your pull requests.
* [Coding principles](https://github.com/DEFRA/software-development-standards/blob/master/principles/coding_principles.md) also apply to QA.

## The GitHub process

This guidance is based on the [software development standards for pull requests](https://github.com/DEFRA/software-development-standards/blob/master/processes/pull_requests.md), tailored to a QA audience.

These are the most common steps for updating a test repository, using the command prompt. The examples assume that you're working on a branch called `feature/add-accessibility-page` in the `qa-test` repository, which is in your local `projects` folder.

### Make sure you have the latest code

Start the command prompt, navigate to your project folder and pull the code from the repository:

```bash
cd projects/qa-test
git pull
```

This doesn't overwrite any code you've already written on your machine. If you don't do this then you're much more likely to have conflicts to deal with later.

### Set up a new branch

Go to the [repository's page on GitHub](https://github.com/DEFRA/qa-test) and create a new branch. Give it a descriptive name based on what you're planning to work on, for example, "feature/add-accessibility-page".

You then need to switch to the branch on your machine, and ensure that the changes you make on your machine stay in sync with the changes on the same branch in Git:

```bash
git checkout -b feature/add-accessibility-page
git pull
git branch --set-upstream-to=origin/feature/test-all-links​
```

The `git pull` in the middle is useful because it prompts you to do the "set upstream" step afterwards.

### Update your code

Update your tests, saving regularly to your local machine. When you've reached a natural break, then you can commit (save) the changes and push them to Git.

At regular intervals, it's useful to check the status of what's going to be committed. `git status` is always useful if you're lost.

A common mistake is to forget to add any new files to the commit. If you’ve created any files, add them.  If you don't do this, the new files won't be committed.

The following steps add any new files, check the status,  commit the changes with a message and then push the code to Git. You don't have to keep checking the status, but it's useful to see where you are the first few times:

```bash
git add -A
git status
git commit -a -m "Add a new accessibility page"
git push -u origin feature/add-accessibility-page
git status
```

Some abbreviations:
* `-A` means "all files"
* `-a` means "all modified or deleted files"
* `.` means "any changed files"
* `-u` means "upstream"

### Create a pull request

A pull request (PR) is asking your colleagues if they're happy for you to pull your changes into the `master` branch of the repository. As [master is always shippable](https://github.com/DEFRA/software-development-standards/blob/master/principles/coding_principles.md), it's your responsibility to ensure that the code works beforehand.

Before you raise a pull request, you therefore need to:
* Ensure that all of your tests pass.
* 'Lint' your code. This is like a spelling and grammar check that your code is good enough to go live with. How you do this depends on the framework you use. For Ruby-based frameworks we do this with Rubocop (`bundle exec rubocop`) which points out code issues and tells you how to fix them. You can also install inline linting tools in your text editor.
* Remove any "work in progress" tags as they can cause any Continuous Integration built into GitHub to fail.

If you've made any changes as a result, then commit and push them to your branch.

You can then:
* Navigate to the branch on GitHub
* Click "Compare and pull request"
* Resolve any conflicts that appear
* Add a brief comment explaining why you're making the changes
* Review any automated checks that GitHub carries out on the repository. If they fail, then check the logs and discuss with a colleague if unsure.
* Create the pull request
* Nominate a reviewer (it's polite to talk to them too!)

If your colleagues suggest changes, then you can make these, commit and push to the branch in the same way that you did before, double-checking that your tests still pass.

### Merging your code

Once your colleagues are happy with the code and all automated checks pass, you can then `squash and merge` the code on the pull request page.

You should then take the opportunity to delete the branch you worked on.

To help prevent the code getting out of sync on your local machine, you should then also switch to `master` and pull the latest code:

```bash
git checkout master
git pull
```

You should then switch to a new branch when you start a new piece of work.

### If things go wrong

Sometimes, Git and your computer can get out of sync. If pulling the latest code doesn't help then save a copy of your repository elsewhere on your machine, and try the following:

```bash
git reset --hard origin/master
```

If this doesn't work then delete your repository from your machine and clone the fresh code from GitHub.

Committing little and often, and keeping your pull requests small are the safest ways to prevent things going wrong.

## Masking passwords

Never publish passwords or any other sensitive data to GitHub. Even if you remove them later, GitHub stores all old versions of code, so they're still accessible.

As automated tests often rely on login details however, you need a way to send passwords to your tests. How you do this depends on your framework, but there are two main methods:

### Method 1: Environment variables

Your framework may allow you to pass in passwords as environment variables to your test. On a Mac, this means updating your .bash_profile file to include the variables, and calling them from your tests.

### Method 2: Exclude the config file from Git

You can put passwords in a config gile, then set a .gitignore file in your repository to exclude your config files from commits.

Whichever method you use, speak to a colleague who has done something similar, who can advise on the best way to do this.


## GitHub guides

* [GitHub Hello World tutorial](https://guides.github.com/activities/hello-world/)
* [Using Git with Terminal](https://github.com/codepath/ios_guides/wiki/Using-Git-with-Terminal)
