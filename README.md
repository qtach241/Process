# Maintainer

1. Create the remote repository on Github...

2. Create the local repository...

$ git clone [repo url] [name]
$ cd [name]

3. Create branches for development...

$ git branch integration master
$ git branch dev_name1 integration
$ git branch dev_name2 integration
$ git push -u origin integration
$ git push -u origin dev_name1
$ git push -u origin dev_name2

4. When work on the integration branch is ready to be released, merge the integration branch into the master branch. Master should only contain merge commits...

$ git cd master
$ git merge integration

# Developer