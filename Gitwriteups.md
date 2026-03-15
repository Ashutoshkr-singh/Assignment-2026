# Kabir Git Assignment - 13/13 Exercises
Writeups: master→fix-old-typo solved

Used this Commands for cloning in the gitbash to solve the Exercise ⬇️
git clone https://gitexercises.fracz.com/git/exercises.git
cd exercises
git config user.name "Ashutosh kumar singh"
git config user.email "idfor2025@gmail.com"
./configure.sh
git start



1. just used git start master and then git verify

2. used git A.text to add in stage area then commited it using git commit -m "solved hai"

3. removed one file using git reset A.txt then commited the remaining one using git commit -m "solved"

4. .gitignore created using touch .gitignore and then added instruction *.exe , *.o , *.jar , libraries/ then commited the file

5. used git merge escaped

6. first used  git merge another-piece-of-work to see the conflict then remove the error using vim equation.txt then commited the file

7. git stash then remove the bug through vim file.txt then file then git stash pop and again the added the line given and finally commited

8. used git rebase hot-bugfix

9. git rm --cached ignored.txt to remove then git commit -am "Removed"

10. git mv File.txt file.txt to change file name then commited the file

11. vim file.txt to fix the typo then  git commit -a --amend and proper commit message

12. used git commit --amend --no-edit --date to set the requirement 

13. git rebase -i HEAD~2 then vim file.txt to edit the file then resolved the conflict which arised after  git rebase --continue  after that finally commited the file 
