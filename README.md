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
