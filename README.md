# Quality assurance and test in Defra

How we do quality assurance and testing in Defra (the UK's Department for Environment, Food and Rural Affairs).

This is a holding page - we are trialling putting information on GitHub.

## Pages

[Accessibility](https://github.com/DEFRA/dst-guides/blob/master/process/accessibility.md)

## Why GitHub?

We work in the open by default and GitHub is the easiest way to do this. It has the advantages of being:

* free (unlike Confluence)
* secure (unlike free Google Docs)
* open to all (unlike Sharepoint or an intranet)
* accessible from off-network machines (also unlike Sharepoint)
* easily to collaborate on (unlike an intranet)

The main disadvantage of GitHub is that it is not supported in Internet Explorer. It should still be usable but if you can, we recommend accessing it through Chrome.

## How to edit these pages

### Setup

It is recommended that you have a little bit of GitHub and command line knowledge before starting. Using these can appear daunting at first but it becomes easy and intuitive with practice. It's also the same tool used by our developers and designers.

If you're new to GitHub then the [GitHub Hello World tutorial](https://guides.github.com/activities/hello-world/) is worth doing. The [Defra Digital Service Team guides](https://github.com/DEFRA/dst-guides/tree/master/github) also contain a lot of useful information.

You will need:

* A [GitHub](https://github.com/) account
* Access to push to this repository - contact Andrew Hick or Charlie Beckett
* A command line tool such as Terminal on Mac (built in) or [git bash](https://gitforwindows.org/) on Windows
* A text editor such as [Atom](https://atom.io/)
* A means to upload to GitHub. You can use the command line directly, or an app such as [GitHub Desktop](https://desktop.github.com/).

Once you have these then:

* Navigate to the root folder in your command line with `cd ~`
* Create and navigate to a projects folder: `mkdir projects` and `cd projects`
* Copy the latest code with `git clone https://github.com/DEFRA/qa-test.git`
* Navigate to the prototype folder: `cd qa-test`
* [Set up Git on your machine](https://help.github.com/en/articles/set-up-git)

### Making changes

This section assumes that you are using bash/terminal to upload to GitHub. If you prefer, you can use [GitHub Desktop](https://desktop.github.com/) to pull, commit and push code.

* In your project folder, pull the latest code using `git pull`
* Create a branch from the [repository page](https://github.com/DEFRA/qa-test). Give it a descriptive name for example, "add-accessibility-page". This means that your changes won't conflict with anyone else's.
* Make your changes. Pages are written in [Markdown](https://guides.github.com/features/mastering-markdown/) format.
* If you've created any new files, then add them using `git add -A`
* Commit your changes using `git commit -a -m "A message to say what you're committing"`
* Use `git push -u origin branchname` to push your changes, replacing branchname with the name of your branch.
* Once you're happy with your updates and nothing is broken, then raise a pull request (from the GitHub page for your branch) to ask your colleagues to review your changes. [Pull request guidance](https://github.com/DEFRA/dst-guides/blob/master/process/pull_request.md)
