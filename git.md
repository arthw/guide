### Remove tailed space in file
sed -i 's/[[:space:]]*$//' FILE

### Syncing a fork
Sync a fork of a repository to keep it up-to-date with the upstream repository.

Configure a remote that points to the upstream repository in Git.

1. Open Terminal.
2. List the current configured remote repository for your fork.
```
    $ git remote -v
    > origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    > origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
```
3. Specify a new remote upstream repository that will be synced with the fork.
```
    $ git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```
4. Verify the new upstream repository you've specified for your fork.
```
    $ git remote -v
    > origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    > origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
    > upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
    > upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```

Sync repo:
Fetch the branches and their respective commits from the upstream repository. Commits to master will be stored in a local branch, upstream/master.
```
    git fetch upstream
    git checkout master
    git merge upstream/master
```


### set client ssh key to git server
cat ~/.ssh/id_rsa.pub | ssh git@nas "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"

### remove big file (*.iso) in history

```
cd project
git filter-branch --index-filter 'git rm --cached --ignore-unmatch *.iso' HEAD
```
