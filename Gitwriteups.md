# Kabir Git Assignment - 13/13 Exercises


Setup Commands:

git clone https://gitexercises.fracz.com/git/exercises.git
cd exercises
git config user.name "Ashutosh kumar singh"
git config user.email "idfor2025@gmail.com"
./configure.sh
git start


 1. master
  Command : "git start master" → "git verify"

  Started on master branch, nothing to change. Just verified it directly. The point was to confirm the starting state is fine as it is.



 2. commit-one-file
Commands: "git add A.txt" → "git commit -m "solved hai"

Had two files but only needed to stage and commit one. Used "git add" specifically for A.txt so the other file stays untracked.



 3. commit-one-file-staged
Commands:" git reset A.txt " → "git commit -m "solved" "

Both files were already staged. Used " git reset" to unstage A.txt, then committed only what was left. Reset here doesn't delete anything, just removes from staging area.



 4. ignore-them
Commands: "touch .gitignore" → added `*.exe`, `*.o`, `*.jar`, `libraries/` → `git commit`

Created a .gitignore file and wrote rules to ignore compiled files and the libraries folder. Git reads this file automatically and skips anything matching those patterns.



 5. chase-branch
Commands: "git merge escaped "

The branch `escaped` had commits that master was missing. One merge command brought all those commits into the current branch and fast-forwarded to it.



 6. merge-conflict
Commands: "git merge another-piece-of-work" → `vim equation.txt` → `git commit`

Merging caused a conflict in equation.txt because both branches changed the same line differently. Opened the file in vim, removed the conflict markers, kept the correct version, then committed to finish the merge.



 7. save-your-work
Commands: "git stash" → `vim file.txt` (remove bug) → `git stash pop` → added required line → `git commit`

Had uncommitted work but needed to fix a bug first without losing it. Stashed the work to clean the working directory, fixed the bug, then popped the stash back to restore the original changes and committed everything.



 8. change-branch-history
Commands: "git rebase hot-bugfix"

Needed the current branch to start from hot-bugfix instead of where it originally branched off. Rebase replays the commits on top of the new base, making the history look like it always came from there.



 9. remove-ignored-file
Commands: `git rm --cached ignored.txt` → `git commit -am "Removed"`

The file was already being tracked even though it should have been ignored. `--cached` removes it from tracking without deleting it from disk, then committed to make that removal official.



 10. case-sensitive-filename
Commands: `git mv File.txt file.txt` → `git commit`

Just renaming the file through the OS wouldn't work because Git (especially on Windows/Mac) might not detect the case change. Using `git mv` forces Git to register it as a rename properly.



 11. fix-typo
Commands: `vim file.txt` (fix typo) → `git commit -a --amend`

Fixed the typo in the file then used `--amend` to update the last commit instead of making a new one. Also changed the commit message to something proper at the same time.



 12. forge-date
Commands: `git commit --amend --no-edit --date="<required date>"`

Used `--amend` with `--date` flag to change the timestamp on the last commit. `--no-edit` kept the message same, only the date got updated.



13. fix-old-typo
Commands: `git rebase -i HEAD~2` → `vim file.txt` → resolved conflict → `git rebase --continue` → commit

Needed to go back and fix a typo in an older commit, not the latest one. Used interactive rebase to edit that specific commit, fixed the file, then a conflict came up when continuing — resolved it manually and let the rebase finish.
