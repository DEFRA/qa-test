# How to edit these pages

It is recommended that you have a little bit of GitHub and command line knowledge before starting. Using these can appear daunting at first but it becomes easy and intuitive with practice.

## Setup

Follow the [setup steps on the GitHub page](/github/github.md).

## Making changes

With GitHub, we should usually work on a branch of the main repository in order to prevent conflicts. However, as we are not dealing with production code or making frequent changes, we can follow a simplified version of the flow without branching.

However, take care to ensure that your changes are correct before you push them, especially if you're deleting anything.

You won't need the terminal commands if using GitHub Desktop.

* In the folder for this repository, pull the latest code. (`git pull`)
* Use [Markdown](https://guides.github.com/features/mastering-markdown/) to make your changes.
* If you've created any new files, then add them. (`git add -A`)
* Commit your changes with a concise message. (`git commit -a -m "A message to say what you're committing"`)
* Push your changes. (`git push -u origin master`)

The detailed GitHub process is on the [GitHub](github.md) page.
