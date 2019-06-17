# qa-test

How we do quality assurance and testing in Defra (the UK's Department for Environment, Food and Rural Affairs).

This is a holding page. We work in the open by default, so we are trialling putting information on Github.

This has the advantages of being:
* free
* secure
* open to all
* accessible from home and off-network laptops
* easily editable with a built-in review process

## Pages

[Accessibility](https://github.com/DEFRA/dst-guides/blob/master/process/accessibility.md)

## How to edit

### Setup

It is recommended that you have a little bit of GitHub and command line knowledge before starting. The [Digital Service Team guides](https://github.com/DEFRA/dst-guides/tree/master/github) contain a lot of useful information. Using GitHub can appear daunting at first but becomes easy and intuitive with practice:

You will need the following:

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
* Configure your terminal to access your Git account.

### Making changes

This section assumes that you are using a bash terminal to upload to GitHub.

* In your project folder, pull the latest code using `git pull`
* Work from a branch and create pull requests rather than committing directly to `master`. This encourages peer review and reduces the risk of code conflicts. [Pull request guidance](https://github.com/DEFRA/dst-guides/blob/master/process/pull_request.md)
* Create a branch from the [repository page](https://github.com/DEFRA/qa-test)
* If you've created any new files, then add them using `git add -A`
* Commit your changes using `git commit -a -m "A message to say what you're committing"`
* If nothing is broken, use `git push -u origin branchname` to push your changes.
* If you're working from a branch then replace `master` with the name of your branch.
