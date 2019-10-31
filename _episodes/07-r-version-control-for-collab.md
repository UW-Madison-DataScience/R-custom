---
title: "R version control for collaboration"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---


In the last lesson, we learned how to collaborate with someone by giving
them collaborator access to our repository.
In this lesson, we will learn how to suggest changes to a repository we don't own.

First we will navigate to the github repository we want to make a suggestion to.
In this case we will be adding a country to a group repository.

![Upstream Countries Repo on Github](../fig/01-upstream_contries_ghrepo.png)

The first ting we need to do is "fork" the repository.
This means we will make a copy of this repo that we have access to modify.
We will click the "Fork" button in the upper right hand of Github.

![Forking the repository](../fig/02-forking_repo.png)

Next we need to get a copy of this repository on our local machine (and in Rstudio).
We need to go back to the original repository, which is linked under the repo name.
We can clone the repository by copying the link under the "Clone or download button"

![Clone button on upstream repo](../fig/03-upstream_clone_button.png)

In R studio we will start a new project and choose the "Version Control" option.

![Version control project in Rstudio](../fig/04-cloning_to_rstudio.png)

Next we will tell it to expect a git repository.

![Git button for version control in Rstudio](../fig/05-cloning-choosing-git.png)

Finally we will paste the URL, give the project a name (or leave blank to keep
the repo name), and tell it which folder to put the project in.
This will copy down the repository to our local computer.

![Entering URL for git repo](../fig/06-cloning-pasting-url.png)

Now we have the repository as a project in Rstudio.
This repo has been setup with a `.gitignore` and `README.md` file.

![Cloned repo in rstudio project](../fig/07-cloned_repo_in_rstudio.png)

Now our repository a connection to the main version of this repository
but we also need it to have a connection to our fork of the repository.
First we click the "New Branch" button in the git tab.

![New branch button in rstudio](../fig/08-adding_myfork_remote1.png)

We can then click the "Add Remote..." button to add our fork as a
remote.

The 'origin' remote is the one we cloned the repo from originally,
in this case the main repository.
We will need to switch back to our fork and copy the URL from the
"Clone and Download" button again.

![Forked repo of countries clone button](../fig/09b-copying-myfork-url.png)

Let's call this remote "my_fork", then paste the URL to our fork of
the repo, and press the "Add" button.

![Adding remote button in Rstudio](../fig/10-adding_url_to_fork_in_rstudio.png)

Before we make our changes we want to be sure we have the latest version of
the main repository.
It turns out, since we cloned it one of our colleagues
added a file to the repository.

![New file added to the main repo](../fig/11-see_new_file_in_upstream.png)

We can use the git tab to pull down the latest changes.

![Pulling down latest changes](../fig/12-update_local_copy_by_pulling.png)

We can see the new file in the file panel of Rstudio.

Before we make the changes, let's make a new branch to work in.
This way we can keep the master branch in line with the main repo.
We can make a new branch using the "New Branch" button in Rstudio.

![](../fig/13a-make_new_branch_to_work_in.png)

We then will give our branch a new name.  I'll be add the country
France to the repository so I'll all my branch "AddFrance".
Be sure choose the remote "my_fork" since that is where we will
want to push the changes to when we are done.
Then we can click "Create".

![Pushing the new branch to my_fork remote](../fig/13b-make_new_branch_to_work_in.png)

Next we can use Rstudio as a text editor and look at the united states file.

![United States file](../fig/14-open_united_states_file.png)

We can then make a new country file and update the information.
You may need to look up the information for you country in the web browser.

![Adding France file](../fig/15-make_france_file.png)

We can then save and stage the file.

![Staging France file](../fig/16-stage_france_file.png)

We can then commit the new file we added.

![Committing the France file](../fig/17a-commit_france_file.png)

![The commit being saved to the git repo](../fig/17b-commit_france_file.png)

Then we can push those changes to our fork.

![Pushing changes to fork](../fig/18-push_updated_file.png)

Now when we look at github we can see that there is a new branch.
Github prompts us to compare and make a pull request.

![New branch on github](../fig/19-see_new_branch_on_myfork_ghrepo.png)

<!--- ![](../fig/19-see_new_branch_on_upstream_ghrepo.png) -->

Then we can fill in the information to submit the pull request.

![Making pull request in github](../fig/20-make_pr.png)

Then the person who owns the repo can look at the pull request and make edits.

![Submitted pull request on github](../fig/21-submitted_pr.png)

In our case our collaborator asked us if we could add the largest city to this file.

![Asking for largest city](../fig/22-ask_for_largest_city.png)

If we update the same branch we used in our pull request on our local machine
and push it to our fork, it will update the pull request.

![Adding largest city](../fig/23-adding_largest_city.png)

We then need to stage and commit the changes.

![Committing the largest city changes](../fig/25a-committing_largest_city.png)

<!--- ![](../fig/25b-committed_largest_city.png) -->

We can then push the changes to the repository.

![Pushing to the repository again](../fig/26-pushing_new_commit_to_pr.png)

Now we can see the new commit on our pull request.

![New commit on updated pull request](../fig/27-updated_pr.png)




{% include links.md %}


