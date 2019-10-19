## Contribution Flow

1. Go to your local cloned repository folder. If it's the first time you clone a repo consult [GitHub documentation](https://help.github.com/en/articles/cloning-a-repository).

`cd ~/repo-path/Worthy-v2`

2. Check out to branch `develop`

`git checkout develop`

3. Pull current version

`git pull`

4. Create a new branch from develop with a name relevant to your task `task-name` and checkout at it

`git checkout -b task-name`

5. Perform your task modifying, adding or deleting files in a local repository

6. Add all changes including newly added non-tracked files to commit (empty folders will not be included)
- adding a non-empty `new-folder` requires explicit addition: `git add new-folder`
- to add all files (including in folders): `git add -A`

7. Commit your changes with a meaningful message. If this commit resolves an issue mention it in commit message with `resolves #[issue number]`

`git commit -m "meaningful message. Resolves #13"`

8. Push your commit to remote repository
- first time you push to set up remote tracking `git push -u origin task-name`
- after initial push this is sufficient `git push`

9. Go to GitHub repository and add a pull request to merge your `task-name` branch into `develop`
- on main repository page `Your recently pushed branches:` > `Compare & pull request`
- or go to your `task-name` branch and right to branch name `New pull request`
- choose base branch `develop`
- leave a comment, if PR resolves an issue mention it in description with `resolves #[issue number]` or `fixes #[issue number]`
- press `Create pull request` button.

10. Non-submitter admin reviews open pull request by choosing `Review changes` > `Approve` > `Submit review` after he checked the following:
- changes are not destructive
- feature branch is being merged into `develop`

11. Any admin afterwards can `Squash and merge` the request

12. After the branch is merged it can be safely deleted with `Delete branch` on the same page. If merged branch requires further changes/review it can be left active and deleted later when no longer needed.

## Release Flow
13. Release feature-list and known issues are documented into `documentation/release-notes/release-notes-x.x.md` file from changes in `develop` that are ready to go into production.

14. Pull request from `develop` into `master` is submitted and approved using the flow from steps 9-11.

15. Code is deployed to production automatically.

## Branch names and meaning
`master` - code version currently in production

`develop` - completed code under integration testing (feature branch should be tested before merged into develop)

`task-name` - feature branch, created for any logical piece of the project (issue/task)
