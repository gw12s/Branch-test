# Branch-test
Testing branches, pull, push, commit, etc. 

1. Clone remote repo (GitHub repo) to local repo (computer)

2. Added Activities for Creating, Protecting, Branching in GitHub to Branch-test

# Create a Repository

Create a Github repository and add group members as collaborators.

## Instructions

* One group member should create a new Github repository. Don't worry about the project name now, this can be changed later.

* From the repo's main page, click the "Settings" tab.

* Once in the repo's settings, select the "Collaborators" menu item on the left.

* From the "Collaborators" page, invite your group members to be project collaborators by entering their Github usernames one at a time.

* Each invited group member should receive an email they must open to accept the invitation.

# Students Do: Protect Master Branch

In this activity, we will protect our repo's master branch.

## Instructions

* Only one member per project group needs to complete this activity. 

* Navigate back to the repo's "Settings" page and then select "Branches" from the left sidebar.

* Under "Branches" select "Add rule"

* Branch name pattern: "master" (or name of the branch you want to apply the branch protection rules to)

* You should be presented with some options, check off the following:
! [branch-protection-options](Images/branch-protection-options.png)

* If completed successfully below image should appear and no one should be able to push directly to the master branch. Instead, all changes must be made in the form of pull requests that are to be reviewed by another group member.

! [branch-protection-complete](Images/branch-protection-complete.png)


# Git Branching/Pushing

Create a new branch, implement a feature, and then submit a pull request back into master. We will also cover reviewing pull requests and merging them into master.

# Instructions

## Part I: Branching and Submitting a Pull Request

* In this section, we will create a branch, add a feature, and submit a pull request. **Only one group member should complete this section, everyone else should observe.**

* Run the following command in your terminal to create and checkout to a new branch:
    * "-b" creates the new branch
  `git checkout -b new-branch`
  

* You should now be on a new branch named "add-new-python-script." In order to verify that this worked, run the following command in your terminal:

  `git branch`

* You should see two branches listed: `master` and `add-new-python-script`. The `add-new-python-script` branch should have an asterisk to the left of it. This indicates that this is the branch you're currently on.

* At the root of the repo, create a new file named `data_collection.py`. Inside this file, add code to import the `requests` library and save.

* In your terminal, add and commit the changes. Then push up your code by running following in your terminal:

  `git push origin add-new-python-script`

* This should push up your code to to GitHub on a branch with the same name (`add-new-python-script`).

* Go to the main repo page at github.com and you should see an button that says "Compare & pull request." Click this.

* On the next screen, add a description of the work that was done in the text area and click the "Pull Request" button.

* If completed successfully, you should see the pull request listed under the repo's "Pull request" tab.

## Part II: Reviewing a Pull Request

* In this section, we will review the pull request from Part I and merge it into master. **A different project member should complete this section while others observe**.

* Clone the repo to your computer if you haven't already done so and use the cd command to get into it.

* First, you will want to test the changes introduced by the `add-new-python-script` branch locally. To examine the new branch on your local machine, run the following commands in your terminal:

  `git fetch --all`

  `git checkout add-new-python-script`

* This code should bring the copy of the `add-new-python-script` branch that's on GitHub onto your computer.

  * Make sure this worked by verifying that there's an `data_collection.py` file in your local repo.

  * Normally you'd run the code here to make sure everything works properly.

* Check back out to your local `master` branch by running the following in your terminal:

  `git checkout master`

* Now go to your GitHub repo's main page and go to the "Pull request" section. Select the `add-new-python-script` pull request from the list.

* At the next page select the option to see the "Files changed."

* You should be presented with all of the files that were changed in this PR along with line numbers for any code added or removed.

* If there are any changes you would like made, you can click the line number to leave a comment the PR author will see and should address before approval. Otherwise click "Review changes" and approve the PR. You should be taken to a screen with an option to "Merge pull request." Click this button.

* Once complete, you can delete the feature branch from your machine by running the following in your terminal:

  `git branch -D add-new-python-script`

* Ask an instructor or TA if you get stuck or have any questions!


### EXTRA NOTES
------
Default branch
The default branch is considered the “base” branch in your repository, against which all pull requests and code commits are automatically made, unless you specify a different branch.
The default branch is set to master. To change this setting, add another branch.
