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

1. Clone the repository...

$ git clone [repo url] [name]
$ cd [name]

2. Checkout the (1) integration branch, and (2) your personal development branch...

$ git checkout -b integration origin/integration
$ git checkout -b [dev_name] origin/[dev_name]

3a. Add/modify files and commit them on your personal development branch when ready...

$ git status
$ git add [file_name]
$ git commit -m 'added new file: [file_name]'

3b. (Optional) Back up your personal development branch by pushing it to the remote repository...

$ git push origin [dev_name]

4. When ready, 'sync' and 'reintegrate' your personal development branch with the integration branch. Then push the integration branch so other developers can pull in changes...

$ git checkout integration
$ git pull
$ git checkout [dev_name]
$ git merge integration
$ git checkout integration
$ git merge [dev_name]
$ git push
