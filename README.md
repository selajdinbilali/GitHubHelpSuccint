# GitHubHelpSuccint

## Generate a new SSH key
```$ ssh-keygen -t rsa -b 4096 -C "email@email.com"```

## Adding your SSH key to the ssh-agent
```$ eval $(ssh-agent -s)
$ ssh-add ~/.ssh/id_rsa```

## Adding an existing project to GitHub using the command line

### in the project folder
```$ git init
$ git add .
$ git commit -m "Commit"```

### associate with the remote already created
```$ git remote add origin remoteURL
$ git remote -v```

### push
```$ git push origin master```

## if you forget to add a .gitignore [this stackoverflow answer](https://stackoverflow.com/questions/19663093/apply-gitignore-on-an-existing-repository-already-tracking-large-number-of-files)
### first add you .gitignore
```$ git rm -r --cached .
$ git add .
$ git commit -m ".gitignore is working"```
