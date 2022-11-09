# Git exercise

## Bundle 1

### Exercise 1

```bash

Lenovo@Clever MINGW64 ~/Desktop/git_exercise
$ git init
Initialized empty Git repository in C:/Users/Lenovo/Desktop/git_exercise/.git/

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (master)
$ git branch -m main

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git commit -m"Add Read me file"
[main (root-commit) d3e29ff] Add Read me file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git remote add https://github.com/clever-cr/gitexercise-solutions.git
usage: git remote add [<options>] <name> <url>

    -f, --fetch           fetch the remote branches
    --tags                import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --track <branch>  branch(es) to track
    -m, --master <branch>
                          master branch
    --mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git remote add origin  https://github.com/clever-cr/gitexercise-solutions.git

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (test)
$ git checkout dev
Switched to branch 'dev'
M       README.md

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git branch -D test
Deleted branch test (was d3e29ff).
```

### Exercise 2

```bash

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git status
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

no changes added to commit (use "git add" and/or "git commit -a")

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash
No local changes to save

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash
No local changes to save

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash
Saved working directory and index state WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash pop about.html
error: about.html is not a valid reference

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stach pop about
git: 'stach' is not a git command. See 'git --help'.

The most similar command is
        stash

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash pop about
error: about is not a valid reference

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 6379e9d add git commands
stash@{1}: WIP on dev: 6379e9d add git commands
stash@{2}: WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash pop stash@{1}

bash: it: command not found

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ it stash pop 1
bash: it: command not found

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (b949a7e9b9b63d3960bd2bb533d8849afec874df)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash home.html
fatal: unknown subcommand: home.html

usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash --home.html
error: unknown option `home.html'
usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]

    -k, --keep-index      keep index
    -S, --staged          stash staged changes only
    -p, --patch           stash in patch mode
    -q, --quiet           quiet mode
    -u, --include-untracked
                          include untracked files in stash
    -a, --all             include ignore files
    -m, --message <message>
                          stash message
    --pathspec-from-file <file>
                          read pathspec from file
    --pathspec-file-nul   with --pathspec-from-file, pathspec elements are separated with NUL character


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash -- home.html
Saved working directory and index state WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash list
stash@{0}: WIP on dev: 6379e9d add git commands
stash@{1}: WIP on dev: 6379e9d add git commands
stash@{2}: WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash 0
fatal: unknown subcommand: 0

usage: git stash list [<options>]
   or: git stash show [<options>] [<stash>]
   or: git stash drop [-q|--quiet] [<stash>]
   or: git stash ( pop | apply ) [--index] [-q|--quiet] [<stash>]
   or: git stash branch <branchname> [<stash>]
   or: git stash clear
   or: git stash [push [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [-m|--message <message>]
                 [--pathspec-from-file=<file> [--pathspec-file-nul]]
                 [--] [<pathspec>...]]
   or: git stash save [-p|--patch] [-S|--staged] [-k|--[no-]keep-index] [-q|--quiet]
                 [-u|--include-untracked] [-a|--all] [<message>]


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   team.html

Dropped refs/stash@{1} (500559eb05e7640610a8cc8d51f019173eea87d3)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash -- team.html
Saved working directory and index state WIP on dev: 6379e9d add git commands

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git stash pop 1
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (336b6bc46a6b28d5d5b2a8dd761859fb48327bfe)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git commit -m"add home and about pages"
[dev b578705] add home and about pages
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git push origin development
^C
bash: it: command not found


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git reset --hard
HEAD is now at b578705 add home and about pages
```

## Bundle 2

# Exercise 1

```bash
Lenovo@Clever MINGW64 ~/Desktop/git_exercise (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

no changes added to commit (use "git add" and/or "git commit -a")

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/bundle-2)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/bundle-2)
$ git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   service.html


$ git push origin ft/bundle-2
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 2.39 KiB | 612.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/clever-cr/gitexercise-solutions/pull/new/ft/bundle-2
remote:
To https://github.com/clever-cr/gitexercise-solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```

# Exercise 2

```bash

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/bundle-2)
$ git checkout main
Switched to branch 'main'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
    git branch --set-upstream-to=origin/<branch> main


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git pull
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details.

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream-to=origin/<branch> main


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git pull origin main
From https://github.com/clever-cr/gitexercise-solutions
 * branch            main       -> FETCH_HEAD
Updating d3e29ff..02c030f
Fast-forward
 README.md    | 337 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html   |  12 +++
 home.html    |  12 +++
 service.html |  12 +++
 team.html    |  12 +++
 5 files changed, 385 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html
 create mode 100644 team.html

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$ git commit -m"Service page"
[ft/service-redesign 8491622] Service page
 1 file changed, 2 insertions(+), 1 deletion(-)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 329 bytes | 329.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/clever-cr/gitexercise-solutions/pull/new/ft/service-redesign
remote:
To https://github.com/clever-cr/gitexercise-solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 337 bytes | 337.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/clever-cr/gitexercise-solutions.git
   02c030f..fb77f27  main -> main

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git checkout ft/service-redesign
error: Your local changes to the following files would be overwritten by checkout:
        service.html
Please commit your changes or stash them before you switch branches.
Aborting

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)                              $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign|MERGING)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign|MERGING)
$ git commit -m"resolving conflicts"
[ft/service-redesign 682a677] resolving conflicts

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 219 bytes | 219.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/clever-cr/gitexercise-solutions.git
   8491622..682a677  ft/service-redesign -> ft/service-redesign

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/service-redesign)
$
```

### Bundle 3

# Exercise 1

```bash

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git brach ft/contact-page
git: 'brach' is not a git command. See 'git --help'.

The most similar command is
       branch

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git branch ft/contact-page

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/team-page)
$ git log
commit f713b0535b8b51e140357dc7782e2852faeaf9b2 (HEAD -> ft/team-page, origin/ft/team-page)
Author: clever <cleverumuhuza@gmail.com>
Date:   Mon Nov 7 10:49:30 2022 +0200

   team page

commit f247d5bd253bdc23c6d0a0975caea8cd8934fe79 (origin/ft/service-redesign, ft/service-redesign)
Author: clever <cleverumuhuza@gmail.com>
Date:   Fri Nov 4 15:45:07 2022 +0200

   updating Read me

commit 682a677053b630c092b9e67590e24089f8d660f1
Merge: 8491622 d9538af
Author: clever <cleverumuhuza@gmail.com>
Date:   Fri Nov 4 15:41:05 2022 +0200

   resolving conflicts

commit d9538af27938e7941345c99fd5398487e2c050c9 (origin/main, main, ft/contact-page)
Author: clever <cleverumuhuza@gmail.com>
Date:   Fri Nov 4 15:28:21 2022 +0200

   changes


Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/team-page)
$ git checkout ft/contact-pag
error: pathspec 'ft/contact-pag' did not match any file(s) known to git

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git cherry-pick f713b0535b8b51e140357dc7782e2852faeaf9b2
[ft/contact-page 062f0da] team page
Date: Mon Nov 7 10:49:30 2022 +0200
1 file changed, 12 insertions(+)
create mode 100644 team .html

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git commit -m"contact page"
[ft/contact-page 618cc5f] contact page
1 file changed, 10 insertions(+)
create mode 100644 contactpage.html

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git push origin ft/contact-page
fatal: unable to access 'https://github.com/clever-cr/gitexercise-solutions.git/': Could not resolve host: github.com

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git push origin ft/contact-page
fatal: unable to access 'https://github.com/clever-cr/gitexercise-solutions.git/': Could not resolve host: github.com

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git push origin ft/contact-page
fatal: unable to access 'https://github.com/clever-cr/gitexercise-solutions.git/': OpenSSL SSL_read: Connection was reset, errno 10054

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 713 bytes | 356.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/clever-cr/gitexercise-solutions/pull/new/ft/contact-page
remote:
To https://github.com/clever-cr/gitexercise-solutions.git
* [new branch]      ft/contact-page -> ft/contact-page

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/contact-page)
Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/faq-page)
```

# Exercise 2

```bash
Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git commit -m"main page"
[main 7bed269] main page
 1 file changed, 1 insertion(+)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git push origin main
To https://github.com/clever-cr/gitexercise-solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/clever-cr/gitexercise-solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git push origin main -f
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 293 bytes | 293.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/clever-cr/gitexercise-solutions.git
 + f598c70...7bed269 main -> main (forced update)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/home-page-redesign)
$ git add .

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/home-page-redesign)
$ git commit -m"update home page"
[ft/home-page-redesign f2bdef8] update home page
 1 file changed, 1 insertion(+)

Lenovo@Clever MINGW64 ~/Desktop/git_exercise (ft/home-page-redesign)
$ git push origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 8 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.53 KiB | 523.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/clever-cr/gitexercise-solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/clever-cr/gitexercise-solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
```
