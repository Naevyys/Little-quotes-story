# Little-quotes-story
ADA Data Story website

## Guide to edit the gh-pages branch

The gh-pages branch is protected because the website is deployed from this branch and messing it up happens really fast.
This section is a little guide to explain how to make modifications on this branch via pull requests (need to be reviewed by at least one person).

### Step 1: create a new branch to make your changes

#### On GitHub

1. Navigate to the repository on github.
2. When you arrive in the repo, you will likely be viewing the `main` branch. Change the branch you are viewing to the branch `gh-pages`.
3. Click on the branch and enter the name of a new branch (let's call it `new-branch`) in the text field at the top of the branches list. You will see a text appearing below saying "Create branch: new-branch from 'gh-pages'". Click on this text.
4. Your new branch is created. Now clone the repository with `git clone https://github.com/Naevyys/Little-quotes-story.git` or fetch and pull from it with `git fetch` and `git pull` if you have already cloned from it.
5. You are not done yet! You still need to checkout to your new branch with `git checkout new-branch`\*. The terminal should give you the following messages: 
> Switched to a new branch 'new-branch'
> Branch 'new-branch' set up to track remote branch 'new-branch' from 'origin'.
6. It says that you have created a new branch called `new-branch` locally and that github set its remote origin to be `origin/new-branch` on github. This means that when you will commit and push, it will send your changes to this branch on github.

Now you are done! If you use an IDE, e.g. VSCode, you will likely see the name of the branch you are currently on appear in one of the corners of the window, if you wish to verify on which branch you are. You may need to click somewhere outside of the terminal for the IDE to refresh before you see the new name appearing.

\* Make sure to always commit all your changes before checking out to another branch.

#### Via the commandline

I recommend this way, because it's less of a hassle, especially if you have already cloned the repository. However, it is equivalent to the method via github presented above, so feel free to do whatever you feel more comfortable with.

1. Open a terminal and clone with `git clone https://github.com/Naevyys/Little-quotes-story.git` the repository if not done yet. If you already cloned it, pull from it with `git pull`.
2. Checkout to the branch `gh-pages` by running `git checkout gh-pages`. Pull again with `git pull`. You can skip this step if you were already on the branch `gh-pages`.
3. Create a new branch with the command `git branch new-branch`, where `new-branch` is the name of your new branch. No message in the terminal means the command was successful. If you use an IDE, you can see the name of the branch you are currently on in some corner of the window.
4. Run `git checkout new-branch`\* to switch to your newly created branch. The terminal will give you the following message:
> Switched to branch 'gh-pages'
5. Note here that this branch does not have any remote origin yet, meaning that if you go on github now, you will not see your branch appearing yet. This is normal, your branch was only created locally for now. You will setup this remote origin the first time you want to push commits on github. For now, you can work as usual on your branch.
6. When you want to make your first commit, run `git add your-files` and `git commit -m "your message"` as usual. Then run `git push`. You will get a message like this in your terminal:
> fatal: The current branch new-branch has no upstream branch.
> To push the current branch and set the remote as upstream, use
> 
>    git push --set-upstream origin new-branch
7. This message is telling you that your push did not work, because your branch does not have a remote origin (i.e. an upstream branch) yet, but that you can create it with your push using the command `git push --set-upstream origin new-branch`.
8. This command will setup the remote origin and push your commits. If you now go to github, you will see your new branch appearing in the list of branches. And the next times you will push, `git push` will work without further complications. You are done!

\* Make sure to always commit all your changes before checking out to another branch.

### Step 2: Creating a pull request (PR)

You have been working on your branch (let's call it `your-branch`) and have created something really nice and neat. Now, you would like to deploy it, meaning you want to merge your branch into the branch `gh-pages`. Because you are a github professional now, you create a pull request.

1. Make sure all your changes are committed and pushed on your branch.
2. Navigate to the repository on github and click on the tab `Pull requests`. This will show you the list of open pull requests. In the list header on the right, you will see a button `New pull request`. Click on it. \*
3. You will get a banner with a content like this: `base: main` <- `compare: main`. The `base` is the branch that you want to merge your changes to and `compare` is the branch containing the changes you want to merge. Change the base to `gh-pages` and the compare to `your-branch`. Let's assume that you don't have conflicts, because you likely won't have any. (If you do, let me know, I will do my best to help you.) You will now see a text box appearing.
4. Enter a title for the pull request and a description of the changes you made while working on your branch. Then, on the right, search for the option to add reviewers (should be the first one) and assign at least one person for revision. You cannot assign yourself (sadly). I would recommend you assign everyone else in the group for simplicity, but one other member is enough.
5. Click on `Create pull request`. Your pull request is created!

*Note: In the rule I made, I stated that the PR needed to be approved by at least one person. If you assign more than one person for reviewing, one approval will suffice for the option to merge to become available. We don't have to all approve before we can merge.*

\* IMPORTANT: When you have recently made commits to a branch, you might see a yellow banner with a green button `Compare & pull request`. However, github is configured to merge into the `main` branch by default. If you click on this button, github will suggest you to create a pull request for merging into the `main` branch. You can use this button, but make sure to change the base to `gh-pages` before creating the pull request in this case.

### Step 3: Review and approve a pull request

You have been spammed by one more email stating that your teammate has requested you to review a pull request, so you sight and decide to do it immediately such that you don't have to think about it anymore.

*Note: Informally, you can review any pull request, even if you are not assigned as a reviewer. Formally, as far as I know (but I may be wrong), only an assigned reviewer can approve a PR. This is why I recommend to always assign everyone for now.*

1. Navigate to the repo in the pull requests tab. Click on the pull request you want to review.
2. When you are assigned as a reviewer, you will see a banner on the top suggesting you to review the code. Click on this button.
3. You will see the list of files changed with all changes detailed. Each file has a checkbox on the top right that you can check when you have reviewed it.
4. In case you are unhappy with the changes, don't worry, you can modify things. Just make your changes on the branch for which the pull request was created, commit and push them. The new commits will automatically be added to the pull request, you will see this list of commits under the description of the pull request. Once you are happy with the changes, go check the files again and continue from here.
5. Leave a comment if you want and make sure to check the `approved` option. (I didn't get to make a simulation myself here, because I needed a second person to assign me as a reviewer to do that, so I don't remember the exact names, but it's straightforward when you have it in front of your eyes.) Send your review.

### Step 4: Merging a pull request

You have just approved a pull request or randomly happened to see a PR that was approved by someone, so you want to merge it to finally see the changes!

1. Navigate to the pull requests tab, click on the pull request.
2. Scroll down until you see the merge option. Click on merge.
3. Leave a final message and merge.
4. Optionally, delete the branch. We can create a new one from the new `gh-pages` version of the branch whenever we need. If you do, please notify all people who were working on this branch that it doesn't exist anymore, such that they can checkout to another branch before continuing their work.

You are done! When you navigate to the `gh-pages` branch, you will see all changes from the other branch were merged into the branch. And if you navigate to https://naevyys.github.io/Little-quotes-story/, you will see the new version of the website deployed!

*Note: Github pages may need a few minutes before it deploys the new changes. Be patient, the changes will appear soon.*

## A few useful github commands

* `git status` - Shows you the list of modified files which are added for committing and modified files that are not added for comitting.
* `git diff` - Shows the details of changes in all your non-committed files. You may have to hit `enter` to see the next lines. Examining differences in files is usually much easier using an IDE, but it can be useful when you have nothing else directly at hand.
* `git branch -l` - Displays the list of local branches. Note that these are not the branches on github, these are you local ones! You may have local branches which don't exist remotely (i.e. on github) anymore or don't exist there yet if you haven't setup the upstream.
* `git branch -d your-branch` - Deletes the branch `your-branch` locally.
* ``
