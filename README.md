# Maintainer

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

$ git pull origin integration
$ git checkout [dev_name]
$ git merge integration
$ git checkout integration
$ git merge [dev_name]
$ git push origin integration