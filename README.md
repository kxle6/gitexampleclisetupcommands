###  Create free GitHub account 

https://github.com/

###  Create and use new SSH keys for GitHub account 

https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/

###  If you don't already have Git installed, install it 

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

###  Login with your username/email 

`git config --global user.name “[firstname lastname]”`

`git config --global user.email “[valid-email]”`

###  Make Directory 

`mkdir GitHub`

`cd GitHub`

`mkdir testrepo1`

`cd testrepo1`

###  Initialize Git for local folder 

`git init`

Initialized empty Git repository in /Users/user1/Desktop/GitHub/testrepo1/.git/

###  Create test file 

`touch testfile123.txt`

`ls -la`

total 0

drwxr-xr-x  4 user1  128 Oct 11 12:56 .

drwxr-xr-x  3 user1   96 Oct 11 12:55 ..

drwxr-xr-x  9 user1  288 Oct 11 12:56 .git

-rw-r--r--  1 user1    0 Oct 11 12:56 testfile123.txt

If you have other files you would like to upload to the repo, put them in your /testrepo1 local folder.

###  Verify test file is not added for staging 

`git status`

On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	testfile123.txt

nothing added to commit but untracked files present (use "git add" to track)

###  Add test file for staging 

`git add testfile123.txt` 

If you had multiple files you wanted to upload at once, instead of adding each file individually, you can use the following command to upload all files in the local folder

`git add .`

###  Verify test file is added for staging 

`git status`

On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   testfile123.txt

###  Commit the file to staging 

`git commit -m "First commit"`

[master (root-commit) 72aa07f] First commit

 1 file changed, 0 insertions(+), 0 deletions(-)

 create mode 100644 testfile123.txt


###  After creating a repo on Github.com, point the local working folder to upload to remote repo 

How to create a repo (free acounts only allow for public repo's)

https://help.github.com/articles/create-a-repo/

`git remote add origin https://github.com/<githubusername>/testrepo1.git`

`git push -u origin master`

Username for 'https://github.com': `<githubusername>`

 If you have 2FA for GitHub account, use Token, not password https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/ 

Password for 'https://<githubusername>@github.com': `<password or token>`

Enumerating objects: 3, done.

Counting objects: 100% (3/3), done.

Writing objects: 100% (3/3), 215 bytes | 215.00 KiB/s, done.

Total 3 (delta 0), reused 0 (delta 0)

remote: 

remote: Create a pull request for 'master' on GitHub by visiting:

remote:      https://github.com/<githubusername>/testrepo1/pull/new/master

remote: 

To https://github.com/<githubusername>/testrepo1.git

 * [new branch]      master -> master

Branch 'master' set up to track remote branch 'master' from 'origin'.

###  If you'd like to create and move to a new branch 

`git checkout -b test-branch`

Switched to a new branch 'test-branch'

git branch

  master

* test-branch

###  Push branch to repo  

`git push origin test-branch`

Total 0 (delta 0), reused 0 (delta 0)

remote: 

remote: Create a pull request for 'test-branch' on GitHub by visiting:

remote:      https://github.com/<githubusername>/testrepo1/pull/new/test-branch

remote: 

To https://github.com/<githubusername>/testrepo1.git

 * [new branch]      test-branch -> test-branch

###  Get changes on GitHub back to local folder 

`git pull origin master`

From https://github.com/<githubusername>/testrepo1

 * branch            master     -> FETCH_HEAD

Already up to date.

### More useful commands 

https://education.github.com/git-cheat-sheet-education.pdf