# GIT FLOW
## helps
1. `sudo apt-get install git-flow`
2. `git flow` to know the commands
3. `git flow init` to install base branches and supporting branch prefixes

## feature branch
Q: what is a feature branch?
R: Place where work for a specific feature is done.

helper
1. to clone in the same directory I am: `git clone repo .`
2. `git flow feature start feature-name`
3. every developer after cloning must start git flow: `git flow init`
4. `git flow feature publish featureName` to send to remote repository
5. `git flow feature help` commands to use
6. `git flow feature track featureBranchName` create a new remote tracking branch and switch to that branch, any change can be commit locally, push to remote repository
7. `git push` just to save change to a remote repository
8. `git pull` just to get changes in local repository
9. when done: `git flow feature finish 1-loadingWhenFetch`

## CREATING A RELEASE BRANCH
* what ever bug must be fixed on the release branch and then merged into develop branch
* a release branch is a point in time where a release is ready
* pass to QA

1. git flow release start 'releaseName(sprint1-release)'
2. git flow release publish releaseName(sprint1-release)
3. git flow release track releaseName(sprint1-release)
   1. hubo un cambio en release branch
   2. git commit and git push
4. git checkout develop
5. git pull
6. git merge release/sprint1-release
7. git push

## FINISH THE RELEASE
1. git checkout release/sprint1-release
2. git pull
3. git flow release finish sprint1-release (or tag number) // merge change at master "created sprint1 release"
4. git push --tags
