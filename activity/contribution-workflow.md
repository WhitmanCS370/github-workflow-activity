# Contribution Workflow

## Prepare to work on an issue

In this section you will complete three tasks: find or create and claim an issue, create a feature branch, and open a pull-request back to upstream. All of this you will do before actually working on the feature. Let's quickly discuss why you are doing these tasks before you do them.

Finding or creating and issue and then claiming it helps prevent developers from working on the same thing at the same time. Also issue provide a place for the community to propose and ideas, prioritize issues, size issues, clarify requirements, and verify bugs. So although this step may feel artificial during the activity, it's important to get in the habit of interacting with the community through the issue tracker before doing a significant amount of work.

A branch is a personal copy of the project within a repository. You will create a branch for every issue you work on. This will allow you to work on more than one feature at same time, allowing you to quickly switch between them, while keep their changes separate until you are ready to merge them. This applies to the master branch as well. The master branch contains the official, current copy of the project. Using feature branches allows master to evolve while you work on your features without interfering with your development; and then, when you are ready, you can update your efforts with changes from master. Again, in this activity you might feel branches are artificial and useless. However, when you are working on more significant issues and with more developers branches become invaluable. So we want to practice the full workflow with these more simplistic tasks so that we know what we are doing when things get more complicated.

Last, you will open an empty pull-request back to the organization's repository (upstream). Pull-requests provide a place for developers to discuss their solution design and implementation. By opening a pull-request immediately, you make your efforts visible from the very beginning, allowing others to track progress and provide useful feedback. Getting feedback early may help you avoid pitfalls and will more likely lead to an acceptable solution sooner and with less effort than if you wait until you are "done" to get feedback.

### Find or create, and claim an issue

__Assumptions__

* You are the contributor.
* You are signed into GitHub.

__Instructions__

1. Navigate to your team's repository on GitHub.
2. Click the __Issues__ tab.
3. Search to see if there is an existing issue for what you want to do.
4. If no reasonable issue exists for what you want to do, create one.
5. If someone is assigned to the ticket or has claimed it by leaving a comment that they are working on it, move on, or maybe leave a comment asking about the progress and express interest in working on the issue.
6. If no-one is working on the issue assign yourself to the ticket (or leave a comment that you are working on it).

Congratulations, you now have a claimed issue for the work you plan to do.

### Create a feature branch and a pull request (PR) for your work

__Assumptions__

* You are the contributor.
* You have claimed an issue for the work you plan to do.
* You are signed into GitHub.

__Instructions__

1. First, create a new branch for your work. 
   * Navigate to your team's repository on GitHub. 
   * Where it says "main" near the upper left, open the dropdown menu. 
   * Type the name for your branch and choose "Create branch: BRANCH_NAME from main".

1. Next, commit your first change to this branch.
   * Still on GitHub, navigate to a code file where you plan to make changes.
   * Make sure your new branch is selected.
   * Write a comment (not code!) noting the issue you plan to address.
   * Commit your changes. For the commit message, use "Start BRANCH_NAME".

1. Finally, make a pull request (PR).
   * Still on GitHub, you should now see a big green button that says "Compare & pull request." Click that button.
   * Edit the PR title and comment. Briefly describe what you plan to do, and mention the issue that this PR is addressing. (You can mention the issue by writing `Closes #i`, where `i` is the issue number. When GitHub sees this, it cross-references the issue and the PR allowing folks to easily to get from one to the other. Also, when the PR is merged into master, it will close all issues mentioned this way!)
   * Click the big green button labeled "Create pull request."

Congratulations! You have created a feature branch to hold the changes you will make while working on the issue. You have also opened a PR for this feature branch back to the main branch. This will allow others to follow your progress as you work. Also, the PR is a place where developers can discuss designs and implementations for solutions to issues.

## Work on the issue

__Assumptions__

* You are a contributor.
* You IntelliJ IDEA open.
* You have an open PR associated with the feature branch.

__Instructions__

1. In IDEA, [fetch the new remote branch and check out a local copy](https://www.jetbrains.com/help/idea/manage-branches.html#checkout-Git-branch).
   * If you are iterating on your work and you have already checked out the feature branch, pull changes from GitHub before you start writing code. There may not be any changes, but it's a good habit to get into.
3. Make a small change to the files in your local clone that gets you closer to accomplishing one of your goals (see the activity instructions to remind yourself of what your goals are in this scenario).
4. Test the change to make sure it works. 
5. [Commit your change to the local repository](https://www.jetbrains.com/help/idea/commit-and-push-changes.html#commit). Provide a concise but informative commit message.
6. [Push your change to GitHub](https://www.jetbrains.com/help/idea/commit-and-push-changes.html#push).

Congratulations, you have made a change, committed it to your feature branch, and pushed it up to your fork, which automatically updates the PR associated with your feature branch!

* If you are not done working on the issue, return to [Work on the issue](#work-on-the-issue).
* If you give up, close the PR on GitHub and then go to [Clean up](#clean-up).
* If you think your work is ready to be merged into the main branch, continue to the next section.

## Collaborate to merge your work into the main branch

### Update your PR with changes to the main branch

__Assumptions__

* You are the contributor.
* You IntelliJ IDEA open.
* You have a feature branch and a corresponding PR opened back to the main branch.

__Instructions__

1. [Fetch changes from GitHub](https://www.jetbrains.com/help/idea/sync-with-a-remote-repository.html#fetch).
1. [Merge](https://www.jetbrains.com/help/idea/apply-changes-from-one-branch-to-another.html#merge) the changes from 'origin/main' into your feature branch.
1. If there are conflicts, [resolve the conflicts](https://www.jetbrains.com/help/idea/resolve-conflicts.html). Be sure to test your changes before committing them.
1. Test the merged copy. If there are any problems, return to [Work on the issue](#work-on-the-issue) and continue from there.
1. [Push all changes to GitHub](https://www.jetbrains.com/help/idea/commit-and-push-changes.html#push).

Congratulations, your PR is now up-to-date with the latest changes from upstream. Time to request a review.

### Request a review

__Assumptions__

* You are the contributor.
* You have an open PR.
* You are signed into GitHub.

__Instructions__

1. Navigate to your PR on the team's repository on GitHub.
2. Make a comment. In that comment at-mention one of your team-members who will play the role of _maintainer_ (e.g., `@username`), and ask them to please review your work.
3. Click __comment__ (___do not click___ "close and comment").

 Closing a PR means that it no longer needs to be merged into upstream. As a _contributor_, you would only do this if you are giving up on your effort. More often a PR is closed by the _maintainer_ either when they merge the PR into master or if they decide the PR should never be merged into master (i.e., the PR is no longer relevant, the PR is outside the scope of the project, the PR has been abandoned, etc.).


### Maintainer reviews the PR

__Assumptions__

* You are the maintainer.
* You are signed into GitHub.

__Instructions__

1. Navigate to the PR that needs reviewing on GitHub.
2. Review the changes and make sure they are up to the project's standards. Many projects have style guidelines and acceptance criteria such as "must pass all tests" and "contributions must include unit tests". The maintainer often must merge the contributor's feature branch into master in a local clone and confirm that it works as expected. As this activity is about training contributors, we will not go into the details about how to be a maintainer here.
3. After reviewing the PR, do one of the following (refer to the instructions in the [activity](README.md) for which you should pick)
    * Reject the PR by closing it and leaving a message of why you are closing it.
    * Accept the PR by merging it into master: choose "squash and merge" strategy for now and click __Merge pull request__ and then __Confirm__.
    * Request modifications to the PR if it needs work by leaving a message in the PR indicating what needs to be done.


### Contributor decides what to do next

__Assumptions__

* You are the contributor.
* You have received an automated email notifying you of the _maintainer's_ decision.

__Instructions__

* If the _maintainer_ merged your PR into the master branch in the team repository, go to [Clean up](#clean-up).
* If the _maintainer_ closed the PR without merging (maybe because it's obsolete, or not a feature the maintainer wants, etc.), go to [Clean up](#clean-up).
* If the _maintainer_ asked for adjustments to your work, return to [Work on the issue](#work-on-the-issue) and make the requested changes.


### Clean up

__Assumptions__

* You are the contributor.
* You have a terminal opened in the root of your local clone.

__Instructions__

1. Check out the main branch and pull changes from GitHub.
2. [Delete the feature branch](https://www.jetbrains.com/help/idea/manage-branches.html#delete-branch) from your local repository.

Congratulations, having cleaned up your repositories you have completed this workflow!
