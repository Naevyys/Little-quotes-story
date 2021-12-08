# Little-quotes-story
ADA Data Story website

## Guide to edit the gh-pages branch

The gh-pages branch is protected because the website is deployed from this branch and messing it up happens really fast.
This section is a little guide to explain how to make modifications on this branch via pull requests.

### Step 1: create a new branch to make your changes

#### On GitHub

1. Navigate to the repository on github.
2. When you arrive in the repo, you will likely be viewing the `main` branch. Change the branch you are viewing to the branch `gh-pages`.
3. Click on the branch and enter the name of a new branch (let's call it `new-branch`) in the text field at the top of the branches list. You will see a text appearing below saying "Create branch: new-branch from 'gh-pages'". Click on this text.
4. Your new branch is created. Now clone the repository with `git clone https://github.com/Naevyys/Little-quotes-story.git` or fetch and pull from it with `git fetch` and `git pull` if you have already cloned from it.
5. You are not done yet! You still need to checkout to your new branch with `git checkout new-branch`.
6. Now you are done! If you use an IDE, e.g. VSCode, you will likely see the branch you are currently on appear in one of the corners of the window.

#### Via the commandline


