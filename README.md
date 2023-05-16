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