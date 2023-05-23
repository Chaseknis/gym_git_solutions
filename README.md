# Git Exercise

A git series of exercises

## Bundle 1

### Exercise 1

```bash
chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git init
Initialized empty Git repository in /Users/chaseknis/Documents/The Gym/the_gym_git_exercise/.git/

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git add README.md

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git commit -m 'Initial commit'
[master (root-commit) b5bf04f] Initial commit
 1 file changed, 3 insertions(+)
 create mode 100644 README.md

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git branch -M main

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git remote add origin https://github.com/Chaseknis/gym_git_solutions.git

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git push --set-upstream origin main
Counting objects: 3, done.
Writing objects: 100% (3/3), 247 bytes | 247.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/Chaseknis/gym_git_solutions.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git checkout -b dev        
Switched to a new branch 'dev'

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Chaseknis/gym_git_solutions/pull/new/dev
remote: 
To https://github.com/Chaseknis/gym_git_solutions.git
 * [new branch]      dev -> dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git checkout -b test              
Switched to a new branch 'test'

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git push --set-upstream origin test
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/Chaseknis/gym_git_solutions/pull/new/test
remote: 
To https://github.com/Chaseknis/gym_git_solutions.git
 * [new branch]      test -> test
Branch 'test' set up to track remote branch 'test' from 'origin'.

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git checkout dev
Switched to branch 'dev'
Your branch is up to date with 'origin/dev'.

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git branch -D test
Deleted branch test (was b5bf04f).

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git push origin --delete test      
To https://github.com/Chaseknis/gym_git_solutions.git
 - [deleted]         test
```

### Exercise 2

```bash
chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git status
On branch dev
Your branch is up to date with 'origin/dev'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        home.html

nothing added to commit but untracked files present (use "git add" to track)

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git add .

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash
Saved working directory and index state WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash list
stash@{0}: WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git add about.html

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash
Saved working directory and index state WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash list    
stash@{0}: WIP on dev: e4a9df6 Exercise 1
stash@{1}: WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git add team.html 

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash         
Saved working directory and index state WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash list   
stash@{0}: WIP on dev: e4a9df6 Exercise 1
stash@{1}: WIP on dev: e4a9df6 Exercise 1
stash@{2}: WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html

Dropped stash@{1} (5e248b59b2b6c9b53e2094e6c06d82e5f14ee331)

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash list
stash@{0}: WIP on dev: e4a9df6 Exercise 1
stash@{1}: WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   home.html

Dropped stash@{1} (170a9c00a54d968be127dad26925c534feffed3f)

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git add .

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git commit -m 'Add about.html and home.html files'
[dev 96f2a32] Add about.html and home.html files
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git push
Counting objects: 4, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 559 bytes | 559.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Chaseknis/gym_git_solutions.git
   e4a9df6..96f2a32  dev -> dev

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash list
stash@{0}: WIP on dev: e4a9df6 Exercise 1

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git stash pop stash@{0}                           
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   team.html

Dropped stash@{0} (978ed38d1bb0fb215df6cf642d7fb91b66740c2c)

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % git reset --hard
HEAD is now at 96f2a32 Add about.html and home.html files

chaseknis@Chases-MacBook-Pro the_gym_git_exercise % 
```