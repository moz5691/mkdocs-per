# Git

## Git commands
```shell
$ git diff
$ git status
$ git log --graph --all --decorate
```


### Git stash
Git has 'stash' to store all local changes ready to re-apply at will.
The most use case is:

```text
[do some work]
[get interrupted]
$ git stash
[deal with interruption]
git stash pop
```

```git stash``` commits the state of the index and then commits the local change to the refs/stash branch and merges them as a child of the HEAD on a new refs/stash branch.
```shell
/# mkdir lgthw_git_stash_1
/# cd lgthw_git_stash_1
/lgthw_git_stash_1# git init
Initialized empty Git repository in /lgthw_git_stash_1/.git/
/lgthw_git_stash_1# echo 'Some content' > file1
/lgthw_git_stash_1# git add file1
/lgthw_git_stash_1# git commit -am initial
[master (root-commit) f6ba996] initial
 1 file changed, 1 insertion(+)
 create mode 100644 file1
/lgthw_git_stash_1# echo 'Some changes I am not sure about' >> file1
/lgthw_git_stash_1# git diff
diff --git a/file1 b/file1
index 0ee3895..49a96d6 100644
--- a/file1
+++ b/file1
@@ -1 +1,2 @@
 Some content
+Some changes I am not sure about
```

```shell

$ git stash list  # to see your stash list
$ git stash pop   # when you ready, re-apply those changes on the same codebase
$ git stash show <ID> # get minimal information about stash with ID
$ git stash show --patch <ID> # get information in a different format
$ git stash apply <ID>  # apply change for <ID>
$ git stash drop   # remove the stash items
$ git reflog  # show a history of the changes made to the HEAD
```

### Git rebase

