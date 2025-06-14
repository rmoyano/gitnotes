# Create an initial repository

Brief notes about branches.

1. Initialize the repository and set the new default branch as `main`:
```shell
user@debian:~/gitnotes$ git init -b main
Initialized empty Git repository in /home/user/gitnotes/.git/
```

2. Add user name and e-mail account for a single repository:
```shell
user@debian:~/gitnotes$ git config user.name "Rafael Moyano"
git config user.email "rafa@gmail.com"

Verify that are set:
user@debian:~/gitnote$ git config user.name
Rafael Moyano
user@debian:~/gitnote$ git config user.email
rafa@gmail.com
```

3. Add the `remote` repository to your local GIT repository:
```shell
user@debian:~/gitnotes$ git remote add origin git@github.com:rmoyano/horarios.git

user@debian:~/gitnotes $ git remote -v
origin	git@github.com:rmoyano/horarios.git (fetch)
origin	git@github.com:rmoyano/horarios.git (push)
```

4. Add file to stage:
```shell
user@debian:~/gitnotes$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md
user@debian:~/gitnotes$ git add README.md
```

5. Commit file:
```shell
user@debian:~/gitnotes$ git commit -m 'Readme file created'
[main (root-commit) dfa32b6] Readme file created
 1 file changed, 33 insertions(+)
 create mode 100644 README.md
user@debian:~/gitnotes$ git status
On branch main
nothing to commit, working tree clean
```

6. Push to Github:
```shell
user@debian:~/gitnotes$ git push 
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

user@debian:~/gitnotes$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 878 bytes | 878.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:rmoyano/horarios.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin' by rebasing.
```
