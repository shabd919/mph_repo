# mph_repo

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git branch sh111

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git branch shabd1

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git branch -1
error: unknown switch `1'
usage: git branch [<options>] [-r | -a] [--merged] [--no-merged]
   or: git branch [<options>] [-f] [--recurse-submodules] <branch-name> [<start-point>]
   or: git branch [<options>] [-l] [<pattern>...]
   or: git branch [<options>] [-r] (-d | -D) <branch-name>...
   or: git branch [<options>] (-m | -M) [<old-branch>] <new-branch>
   or: git branch [<options>] (-c | -C) [<old-branch>] <new-branch>
   or: git branch [<options>] [-r | -a] [--points-at]
   or: git branch [<options>] [-r | -a] [--format]

Generic options
    -v, --[no-]verbose    show hash and subject, give twice for upstream branch
    -q, --[no-]quiet      suppress informational messages
    -t, --[no-]track[=(direct|inherit)]
                          set branch tracking configuration
    -u, --[no-]set-upstream-to <upstream>
                          change the upstream info
    --[no-]unset-upstream unset the upstream info
    --[no-]color[=<when>] use colored output
    -r, --remotes         act on remote-tracking branches
    --contains <commit>   print only branches that contain the commit
    --no-contains <commit>
                          print only branches that don't contain the commit
    --[no-]abbrev[=<n>]   use <n> digits to display object names

Specific git-branch actions:
    -a, --all             list both remote-tracking and local branches
    -d, --[no-]delete     delete fully merged branch
    -D                    delete branch (even if not merged)
    -m, --[no-]move       move/rename a branch and its reflog
    -M                    move/rename a branch, even if target exists
    --[no-]omit-empty     do not output a newline after empty formatted refs
    -c, --[no-]copy       copy a branch and its reflog
    -C                    copy a branch, even if target exists
    -l, --[no-]list       list branch names
    --[no-]show-current   show current branch name
    --[no-]create-reflog  create the branch's reflog
    --[no-]edit-description
                          edit the description for the branch
    -f, --[no-]force      force creation, move/rename, deletion
    --merged <commit>     print only branches that are merged
    --no-merged <commit>  print only branches that are not merged
    --[no-]column[=<style>]
                          list branches in columns
    --[no-]sort <key>     field name to sort on
    --[no-]points-at <object>
                          print only branches of the object
    -i, --[no-]ignore-case
                          sorting and filtering are case insensitive
    --[no-]recurse-submodules
                          recurse through submodules
    --[no-]format <format>
                          format to use for the output


shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git branch -l
  SP_123
* main
  sh111
  shabd1
  shabd12

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git checkout SP_123
Switched to branch 'SP_123'

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ ls
First.txt  README.md

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ echo hello>f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git ls-files
First.txt
README.md

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ ls
First.txt  README.md  f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git status
On branch SP_123
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        f1.txt

nothing added to commit but untracked files present (use "git add" to track)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git add f1.txt
warning: in the working copy of 'f1.txt', LF will be replaced by CRLF the next time Git touches it

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git commit -m "creating f1 file"
[SP_123 a19d88d] creating f1 file
 1 file changed, 1 insertion(+)
 create mode 100644 f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git status
On branch SP_123
nothing to commit, working tree clean

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ ls
First.txt  README.md  f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git ls-files
First.txt
README.md
f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 8 commits.
  (use "git push" to publish your local commits)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git ls-files
First.txt
README.md

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git merge SP_123
Updating feb009a..a19d88d
Fast-forward
 f1.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git ls-files
First.txt
README.md
f1.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git checkout sh111
Switched to branch 'sh111'

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (sh111)
$ echo good morning>f2.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (sh111)
$ git ls-files
First.txt
README.md

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (sh111)
$ git add .
warning: in the working copy of 'f2.txt', LF will be replaced by CRLF the next time Git touches it

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (sh111)
$ git commit -m "adding file"
[sh111 66e5fe6] adding file
 1 file changed, 1 insertion(+)
 create mode 100644 f2.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (sh111)
$ git ls-files
First.txt
README.md
f2.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (sh111)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 9 commits.
  (use "git push" to publish your local commits)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git merge sh111
Merge made by the 'ort' strategy.
 f2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 f2.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git ls-files
First.txt
README.md
f1.txt
f2.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git checkout main
Already on 'main'
Your branch is ahead of 'origin/main' by 11 commits.
  (use "git push" to publish your local commits)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git branch -a
  SP_123
* main
  sh111
  shabd1
  shabd12
  remotes/origin/main

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ echo First File>first.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ echo second File>second.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git add .
warning: in the working copy of 'First.txt', LF will be replaced by CRLF the next time Git touches it
warning: in the working copy of 'second.txt', LF will be replaced by CRLF the next time Git touches it


shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git commit -m "created first.txt and second.txt"
[main bff862f] created first.txt and second.txt
 2 files changed, 2 insertions(+)
 create mode 100644 second.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ vim first.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git add .
warning: in the working copy of 'First.txt', LF will be replaced by CRLF the next time Git touches it

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git commit -m "chang1 in first.txt"
[main 638f8ad] chang1 in first.txt
 1 file changed, 1 insertion(+), 1 deletion(-)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ vim second.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git add .
warning: in the working copy of 'second.txt', LF will be replaced by CRLF the next time Git touches it

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git commit -m "chang1 in second.txt"
On branch main
Your branch is ahead of 'origin/main' by 13 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git log --oneline
638f8ad (HEAD -> main) chang1 in first.txt
bff862f created first.txt and second.txt
3a39cc5 Merge branch 'sh111'
66e5fe6 (sh111) adding file
a19d88d (SP_123) creating f1 file
feb009a (shabd12, shabd1) Merge branch 'main' of https://github.com/shabd919/mph_repo
ad76a09 sec
12b971d (origin/main) Create README.md
3dd1824 Creat First
5049d2b Creat First
ad769ab Del
3095b0d modified
f95304e modified
34833c8 First Commit

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git show HEAD
commit 638f8ad214ac4ec9acb892a4924469a58bf7d58b (HEAD -> main)
Author: shabd919 <shabd.prakash1998@gmail.com>
Date:   Mon Aug 5 16:58:33 2024 +0530

    chang1 in first.txt

diff --git a/First.txt b/First.txt
index c9e358c..5c23967 100644
--- a/First.txt
+++ b/First.txt
@@ -1 +1 @@
-First File
+First File changes

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git show HEAD~1
commit bff862fa11aa095ea694c2740076b0744078b47d
Author: shabd919 <shabd.prakash1998@gmail.com>
Date:   Mon Aug 5 16:53:56 2024 +0530

    created first.txt and second.txt

diff --git a/First.txt b/First.txt
index e69de29..c9e358c 100644
--- a/First.txt
+++ b/First.txt
@@ -0,0 +1 @@
+First File
diff --git a/second.txt b/second.txt
new file mode 100644
index 0000000..22dd32e
--- /dev/null
+++ b/second.txt
@@ -0,0 +1 @@
+second File

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git reset --hard Head~1
HEAD is now at bff862f created first.txt and second.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git log --oneline
bff862f (HEAD -> main) created first.txt and second.txt
3a39cc5 Merge branch 'sh111'
66e5fe6 (sh111) adding file
a19d88d (SP_123) creating f1 file
feb009a (shabd12, shabd1) Merge branch 'main' of https://github.com/shabd919/mph_repo
ad76a09 sec
12b971d (origin/main) Create README.md
3dd1824 Creat First
5049d2b Creat First
ad769ab Del
3095b0d modified
f95304e modified
34833c8 First Commit

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ get checkout SP_123
bash: get: command not found

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git checkout SP_123
Switched to branch 'SP_123'

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ touch two.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git add .

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git commit -m "creat two.txt from SP_123"
[SP_123 4cef01a] creat two.txt from SP_123
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 two.txt

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git log --oneline
4cef01a (HEAD -> SP_123) creat two.txt from SP_123
a19d88d creating f1 file
feb009a (shabd12, shabd1) Merge branch 'main' of https://github.com/shabd919/mph_repo
ad76a09 sec
12b971d (origin/main) Create README.md
3dd1824 Creat First
5049d2b Creat First
ad769ab Del
3095b0d modified
f95304e modified
34833c8 First Commit

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (SP_123)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 12 commits.
  (use "git push" to publish your local commits)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git rebase SP_123
Successfully rebased and updated refs/heads/main.

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git log --oneline
8563421 (HEAD -> main) created first.txt and second.txt
2607a19 adding file
4cef01a (SP_123) creat two.txt from SP_123
a19d88d creating f1 file
feb009a (shabd12, shabd1) Merge branch 'main' of https://github.com/shabd919/mph_repo
ad76a09 sec
12b971d (origin/main) Create README.md
3dd1824 Creat First
5049d2b Creat First
ad769ab Del
3095b0d modified
f95304e modified
34833c8 First Commit

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$ git log --pretty='format:%C(auto)%h(%s,%ad)'
8563421(created first.txt and second.txt,Mon Aug 5 16:53:56 2024 +0530)
2607a19(adding file,Mon Aug 5 16:33:01 2024 +0530)
4cef01a(creat two.txt from SP_123,Mon Aug 5 17:35:02 2024 +0530)
a19d88d(creating f1 file,Mon Aug 5 16:06:31 2024 +0530)
feb009a(Merge branch 'main' of https://github.com/shabd919/mph_repo,Mon Aug 5 14:52:54 2024 +0530)
ad76a09(sec,Mon Aug 5 14:52:33 2024 +0530)
12b971d(Create README.md,Mon Aug 5 14:25:18 2024 +0530)
3dd1824(Creat First,Mon Aug 5 14:09:42 2024 +0530)
5049d2b(Creat First,Mon Aug 5 14:07:30 2024 +0530)
ad769ab(Del,Mon Aug 5 13:55:59 2024 +0530)
3095b0d(modified,Mon Aug 5 13:38:00 2024 +0530)
f95304e(modified,Mon Aug 5 13:33:27 2024 +0530)
34833c8(First Commit,Mon Aug 5 11:50:00 2024 +0530)

shabd.prakash@WKSCHE03TRNG041 MINGW64 ~/GitFolder/mph_repo (main)
$
