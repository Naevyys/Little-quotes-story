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
5. You are not done yet! You still need to checkout to your new branch with `git checkout new-branch`. The terminal should give you the following messages: 
> Switched to a new branch 'new-branch'
> Branch 'new-branch' set up to track remote branch 'new-branch' from 'origin'.
6. This means that you have created a new branch called `new-branch` locally and that github set its remote origin to be `origin/new-branch` on github. This means that when you will commit and push, it will send your changes to this branch on github.

Now you are done! If you use an IDE, e.g. VSCode, you will likely see the branch you are currently on appear in one of the corners of the window, if you wish to verify on which branch you are.

#### Via the commandline

I recommend this way, because it's less of a hassle, especially if you have already cloned the repository. However, it is equivalent to the method via github presented above, so feel free to do whatever you feel more comfortable with.

1. Open a terminal and clone with `git clone https://github.com/Naevyys/Little-quotes-story.git` the repository if not done yet. If you already cloned it, pull from it with `git pull`.
2. Checkout to the branch `gh-pages` by running `git checkout gh-pages`. Pull again with `git pull`. You can skip this step if you were already on the branch `gh-pages`.
3. Create a new branch with the command `git checkout new-branch`, where `new-branch` is the name of your new branch. No message in the terminal means the command was successful.
4. Run `git checkout new-branch` to switch to your newly created branch. The terminal will give you the following message:
> Switched to branch 'gh-pages'
5. Note here that this branch does not have any remote origin yet, meaning that if you go on github now, you will not see your branch appearing yet. This is normal, your branch was only created locally for now. You will setup this remote origin the first time you want to push commits on github.
