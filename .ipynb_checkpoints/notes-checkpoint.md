# Notes

- GitHub/GitLab/Bitbucket - all repositories

- unix command line course - might be handy?

- Install GitBash.  When using Windows, git config --global core.autoclrf true (because windows uses different line endings)

- Need to specify a plain text editor.  in this workshop we use nano.

## To start off:

- jupyter-npl71@FREDDIE:~$ git config --global user.name "Penny"
- jupyter-npl71@FREDDIE:~$ git config --global user.email "penny.lawton@newcastle.ac.uk"
- jupyter-npl71@FREDDIE:~$ git config --global core.editor "nano -w"

- *ls -a* reveals hidden files

- *rm -r* removes directories.  If you accidentally initialise a git repo in a subdirectory, use rm -r git to remove it.

- *cat* tells you what's in a file

- Always do a git add before a git commit.  Adding puts the file in the 'staging area', before we commit - a bit like getting on the platform before we get on a train.

- git diff --staged gives us difference between last committed file and file on stage

- q to quit at end in shell (if eg git log is too long) - git log --oneline can give one line updates which is a bit tidier.  git -N gives the last N updates
- git does not add empty directories.  You can add a little empty file in there if you want it added using *touch* command.  Dot creates a hidden file
- git add . adds everything

- ssh - need to create keygen so we can have an id for github (add ssh key).  Use ssh-keygen (no spaces)
- git branch -M main (M is for main.  Some older versions may say master)

- mv renames a file

- ! is an exception in gitignore

## Afternoon stuff

- git checkout switches to a new branch
- git checkout -b creates a new branch and switches directly to it
- git branch -d deletes a branch
- git branch -D overrides this (use with care!)
- Network in github website allows us to look at main and branchy stuff over time (possibly only available on the paid version - check)
- branches can come off branches.  Sometimes don't last very long, few days/weeks.

- do a git pull at least once a week!  If you change the same file and line as someone else, you'll have to fix it, and it'll be messy.
- git config pull.rebase false
- use cat and you'll see what the conflicting doodads are.  Git will add some information to the file, something like <<<<HEAD.  The top repo has the head line in, the other bit is the commit number.  You have to decide which one to keep.  Or just keep both and delete the git bits
- HEAD is the latest thing you've changed.  ~N goes back in the list of stuff N times.
- git show shows state of repo at a particular point in time
- All commits have a unique identifier (a big bunch of numbers and letters).  You can refer to a particular commit by its ID.  The first 7 characters is generally enough.
- git checkout HEAD/unique ID will roll back to an older version.  You can recover old commits this way.  Changes are however kept, so you can go back to them.
- (generally poor practice to wipe out all changes - just roll back instead)
- if you don't add the filename you end up in a 'detached HEAD' state.  *git switch -* to undo the operation (easily done by accident!).  Or create a new branch and commit it

### Pull requests

- provides traceability
- allows you to request that changes are incorporated into a repo that isn't yours
- Cloning makes a separate directory.  Forking keeps a link to the original repository.  