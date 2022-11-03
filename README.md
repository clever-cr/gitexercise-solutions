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
