# Week 1 Goals
  
## Able to use git
* Fork/clone repo
* Pull upstream master
* Create own branches
* Send Pull Requests
* Use cli to submit PRs

### Fork/clone repo
Forking a repository is the same as making a copy of that repository where you will make alterations. To do so:
1. go to the repository you want to contribute (probably in GitHub);
1.  Click on _Fork_.

Now you have a copy of the repository under your GitHub account.

Cloning the repository is the same as copying that repository to your machine so you can work on it:

1. In your forked repository page, click on _Code_;
1. Copy the link in HTTPS;
1. Go to the terminal in your computer and enter this line: `git clone HTTPS-link`

Now you have a copy of the repository on your machine.


### Pull upstream master
When you _pull_ code, you are fetching the latest changes from a certain repository and merging them into your local copy.

We can set the _upstream_ and _origin_ repositories to indicate where we want to get the information from or send the information to.

The upstream repository is the original. The one you forked in the last step. The origin repository is the copy you have under your GitHub account.

To check your current remote repositories you can enter `git remote -v` in your terminal.

To add a remote in your terminal:
1. `git remote add upstream upstream-repo-url` if you want to add the remote upstream to your repository.
1. `git remote add origin origin-repo-url` if you want to add the remote origin to your repository.

    > If you have already cloned your forked repository, the origin reference is automatically set during the cloning process.

You can now use `git pull upstream master` to indicate that you want to fetch all recent alterations from the master branch of your original repository. Then, you can use `git push origin master` o push the alterations to your forked repository.

### Create own branches
Git is a versioning system that we use to track and manage changes to source code during software development. It allows multiple developers to collaborate on a project.

To keep the project organized and maintain a certain order (coding can be pretty chaotic), we can create branches: pointers that represent independent lines of development.

We use branches to make alterations to the code without affecting the master/main version during our development process. Later, we can merge the changes from this branch and deal with possible conflicts.

To create a new branch and move to it:
`git checkout -b new-branch-name`.

We can also move from one branch to the other using `git checkout branch-name`

Once in your branch, you can make alterations, save them, and send them to someone's copy of the repository or the upstream repository itself.

1. Check the alterations you made with `git status`
1. Add the files you altered with `git add .` (if you want to add all the files you altered) or `git add path-to-the-file` (if you want to add a specific file)
1. Commit the changes with a message with `git commit -m "message"`
1. Push the changes to your repository with `git push origin new-branch-name`
1. In your hosting platform you will see a banner indicating that you recently pushed a new branch. (GitHub) Click on the _Compare & Pull request" button to start the Pull Request.

Now someone will review your PR and approve it to be merged.

## Use cli to submit PRs
You can use a command-line interface tool (a text-based interface used to interact with a computer program or operating system by entering commands through a command prompt or terminal) to help perform the Pull Requests.

GitHub has its [own CLI](https://github.com/cli/cli#installation). After you install it, follow the steps from the previous section. After step 4, you can create your PR using the CLI:

`gh pr create --title "Your PR title" --body "Additional description if necessary"`

In Liferay, we use GitRay CLI. You can check Step 13 in [this document](https://liferay.atlassian.net/l/cp/T7rVz4xw) to understand more about it. 

Well, that is it. Now you are able to use git. Congratulations!