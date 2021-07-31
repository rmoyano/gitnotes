# Branches

Brief notes about branches.


1. Create a new branch called *test*: 
```shell
user@debian:~/gitnotes$ git branch test
```

2. Check that it is created:
```shell
user@debian:~/gitnotes$ git branch 
* main
  test
```

3. Let say that you want to modify the new branch *test* to *feature1*:
```shell
user@debian:~/gitnotes$ git branch -m test feature1
```

4. You can create a new branch and switch to that branch with one command:
```shell
user@debian:~/gitnotes$ git checkout -b feature2
Switched to a new branch 'feature2
```
This command would be equivalent to:
```shell
user@debian:~/gitnotes$ git branch feature2
user@debian:~/gitnotes$ git checkout feature2
Switched to a new branch 'feature2
```
5. You can list all the branches created by using:
```shell
user@debian:~/gitnotes$ git branch -a
  feature1
* feature2
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
```
6. After you completed a feature, you will need to delete that branch:
```shell
user@debian:~/gitnotes$ git branch -d feature2
Deleted branch feature2 (was f0d44a7).
```