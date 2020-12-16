# GitHubHelpSuccint

## Generate a new SSH key
```
$ ssh-keygen -t rsa -b 4096 -C "email@email.com"
```

## Adding your SSH key to the ssh-agent
```
$ eval $(ssh-agent -s)
$ ssh-add ~/.ssh/id_rsa
```

## Adding an existing project to GitHub using the command line

### In the project folder
```
$ git init
$ git add .
$ git commit -m "Commit"
```

### Associate with the remote already created
```
$ git remote add origin remoteURL
$ git remote -v
```

### Push
```
$ git push origin master
```

## If you forget to add a .gitignore [this stackoverflow answer](https://stackoverflow.com/questions/19663093/apply-gitignore-on-an-existing-repository-already-tracking-large-number-of-files)
### First add you .gitignore
```
$ git rm -r --cached .
$ git add .
$ git commit -m ".gitignore is working"
```

# Workflow
## Pull
```
$ git pull
```

## Create a branch to add a feature
```
$ git checkout -b newFeature
```

### If this branch last more than one day, push to the remote
```
$ git push --set-upstream origin newFeature
```

## Go back to master and merge
```
$ git checkout master
$ git pull
$ git merge newFeature
```

### If you dont need the branch anymore, delete locally and remotely
```
$ git branch -d newFeature
$ git push origin :newFeature
```

## Cleaner history with rebase
### In master branch
```
$ git fetch
$ git rebase
```
If conflicts
```
$ git rebase --continue
```

## Local merge - fast forward
```
$ git checkout newFeatue
$ git rebase master
$ git checkout master
$ git merge newFeature
```
