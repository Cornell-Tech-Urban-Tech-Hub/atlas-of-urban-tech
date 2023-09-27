# GIT BEST PRACTICES FOR COLLABORATION

## TL, DR;

[This post](https://reflectoring.io/github-fork-and-pull/) is the most concise, comprehensive version on how to collaborate with the "fork and pull" method.
## WHAT's A FORK?

> Forks let you make changes to a project without affecting the original repository, also known as the "upstream" repository. After you fork a repository, you can fetch updates from the upstream repository to keep your fork up to date, and you can propose changes from your fork to the upstream repository with pull requests. A fork can be owned by either a personal account or an organization.
>
> -- [GitHub Help](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/about-forks)

> Moreover, Git Fork establishes a clear workflow for contributing to open-source projects, making it easier for developers to submit their changes for review through pull requests. This process ensures that project maintainers have full control over the changes that get merged into the main repository while still encouraging contributions from the community.
>
> -- [Mastering Git Fork](https://marketsplash.com/tutorials/git/git-fork/)
## WHY IMPORTANT TO KEEP FORKS IN SYNC WITH UPSTREAM

> Pretend that you are working on a fork of your colleague’s repo. Your colleague’s repo is the final home for the code and content that you are working together on collaboratively. Your colleague and others in your group may be updating code while you are working. It is important to ensure that your fork is in sync with your colleague’s repo, ideally before making a new pull request to that repo. Your repo being in sync refers to your fork having all of the commits or changes to the code and files that have been made to the parent repo. 
>
> -- [Blog Post](https://www.earthdatascience.org/courses/intro-to-earth-data-science/git-github/github-collaboration/update-github-repositories-with-changes-by-others/)


## GENERALLY, NO SINGLE BEST WAY

> "Different team uses different workflow."
>
> -- [StackOverflow](https://stackoverflow.com/questions/55501551/what-is-the-standard-way-of-keeping-a-fork-in-sync-with-upstream-on-collaborativ)

## WHAT SEEMS TO BE THE MOST COMMON METHOD

From [Mastering Git Fork: A Comprehensive Guide ](https://marketsplash.com/tutorials/git/git-fork/)

To ensure that your forked repository stays current with the latest changes from the original project, you need to set up a link to the upstream repository and periodically sync your fork. Follow these steps to keep your fork up-to-date:

1. **Add the upstream repository as a remote:** Run the following command to add the original repository (upstream) as a remote. Replace the URL with the original repository's URL.
                
                git remote add upstream https://github.com/ownerusername/original-repository.git

2. **Fetch the latest changes from the upstream repository:** To retrieve the latest changes from the original repository, run: `

                git fetch upstream

3. **Merge the upstream changes into your local branch:**  To First, ensure you're on the branch you want to update (typically the main or master branch). Then, run, replace *main* with the appropriate branch name if the upstream repository uses a different default branch.

                git merge upstream/main

4. **Push the updated branch to your forked repository:** After merging the upstream changes, push the updated branch to your fork on GitHub. Again, replace *main* with the appropriate branch name if needed:

                git push origin main



## A DIFFERENT, POSSIBLY BETTER METHOD: REBASING

https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase

From a content perspective, rebasing is changing the base of your branch from one commit to another making it appear as if you'd created your branch from a different commit. Internally, Git accomplishes this by creating new commits and applying them to the specified base.

https://www.reddit.com/r/git/comments/z01ejf/keeping_a_fork_updated_best_practices/
* this 2022 thread has pretty current and detailed info on rebasing practoice

It's very important for long living feature branches to regularly rebase on master. That would have saved you the head aches now and reduced your work then because the merge conflicts would be smaller and more easily resolved. 


## TRIED + TRUE METHOD = REBASE FORK FROM COMMAND LINE USING UPSTREAM REMOTE

Explained in this [thread](https://stackoverflow.com/questions/7244321/how-do-i-update-or-sync-a-forked-repository-on-github):

        # Add the remote, call it "upstream":

        git remote add upstream https://github.com/whoever/whatever.git

        # Fetch all the branches of that remote into remote-tracking branches

        git fetch upstream

        # Make sure that you're on your main branch:

        git checkout main

        # Rewrite your main branch so that any commits of yours that
        # aren't already in upstream/main are replayed on top of that
        # other branch:

        git rebase upstream/main

If you've rebased your branch onto upstream/main you may need to force the push in order to push it to your own forked repository on GitHub. You'd do that with:

        git push -f origin main

You only need to use the -f the first time after you've rebased.


## ANOTHER WAY OF REBASING


From [Mastering Git Fork: A Comprehensive Guide ](https://marketsplash.com/tutorials/git/git-fork/)

Rebasing your fork involves applying your changes to the latest version of the upstream repository, resulting in a linear history. Rebasing can be useful for keeping your changes up-to-date and maintaining a clean commit history. Here are some tips for rebasing your fork:

1. Fetch the latest changes from the upstream repository using git fetch upstream.
2. Check out your local branch and run git rebase upstream/main, where upstream/main is the branch you want to rebase onto.
3. Resolve conflicts that occur during the rebase.
4. Push your changes to your fork using git push -f origin your-branch-name.


## OFFICIAL GIHUB HOWTO FOR SYNCING A FORK

https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork

n.b. At the end:

        Tip: Syncing your fork only updates your local copy of the repository. To update your fork on GitHub.com, you must push your changes.


## OTHER RESOURCES

- [Pro Git](https://git-scm.com/book/en/v2) - Definitive 2014 e-book.
- [Git From the Bottom Up](https://jwiegley.github.io/git-from-the-bottom-up/) - Book explains the internals of Git.


