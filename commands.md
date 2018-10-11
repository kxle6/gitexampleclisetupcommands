mkdir GitHub
cd GitHub 
mkdir testprivaterepov1
cd testprivaterepov1 
git init

Initialized empty Git repository in /Users/kcreason/Desktop/GitHub/testprivaterepov1/.git/

touch testfile123.txt
ls -la

total 0
drwxr-xr-x  4 kcreason  PALOALTONETWORK\Domain Users  128 Oct 11 12:56 .
drwxr-xr-x  3 kcreason  PALOALTONETWORK\Domain Users   96 Oct 11 12:55 ..
drwxr-xr-x  9 kcreason  PALOALTONETWORK\Domain Users  288 Oct 11 12:56 .git
-rw-r--r--  1 kcreason  PALOALTONETWORK\Domain Users    0 Oct 11 12:56 testfile123.txt

git status

On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	testfile123.txt

nothing added to commit but untracked files present (use "git add" to track)

git add testfile123.txt 
git status

On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   testfile123.txt

git commit -m "First commit"

[master (root-commit) 72aa07f] First commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 testfile123.txt

git checkout -b test-branch

Switched to a new branch 'test-branch'
git branch
  master
* test-branch

git remote add origin https://github.com/kxle6/testrepo1.git
git push -u origin master
Username for 'https://github.com': kxle6
Password for 'https://kxle6@github.com': 

Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 215 bytes | 215.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/kxle6/testrepo1/pull/new/master
remote: 
To https://github.com/kxle6/testrepo1.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.

git push origin test-branch

Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'test-branch' on GitHub by visiting:
remote:      https://github.com/kxle6/testrepo1/pull/new/test-branch
remote: 
To https://github.com/kxle6/testrepo1.git
 * [new branch]      test-branch -> test-branch

git pull origin master

From https://github.com/kxle6/testrepo1
 * branch            master     -> FETCH_HEAD
Already up to date.