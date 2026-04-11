
# LEARN GIT BRANCHING - COMANDOS COMPLETOS



### SEÇÃO: INTRODUCTION SEQUENCE


[1] Introduction to Git Commit

git commit

git commit


[2] Branching in Git

git checkout -b bugFix


[3] Merging in Git

git checkout -b bugFix

git commit

git checkout main

git commit

git merge bugFix


[4] Rebase Introduction

git checkout -b bugFix

git commit

git checkout main

git commit

git checkout bugFix

git rebase main




### SEÇÃO: RAMPING UP


[1] Detach yo’ HEAD

git checkout c4


[2] Relative Refs (^)

git checkout HEAD^


[3] Relative Refs (~)

git checkout HEAD^

git branch -f main c6

git branch -f bugFix c0


[4] Reversing Changes in Git

git reset local^

git checkout pushed

git revert pushed




### SEÇÃO: MOVING WORK AROUND


[1] Cherry-pick Intro

git cherry-pick c3 c4 c7


[2] Interactive Rebase Intro

git rebase -i HEAD~4




### SEÇÃO: A MIXED BAG


[1] Grabbing Just 1 Commit

git rebase -i HEAD~3

git branch -f main c4'


[2] Juggling Commits

git rebase -i HEAD~2

git commit --amend

git rebase -i HEAD~2

git branch -f main c3''


[3] Juggling Commits #2

git checkout main

git cherry-pick c2

git branch -f main c1

git cherry-pick c2' c3


[4] Git Tags

git tag v0 c1

git tag v1 c2

git checkout c2


[5] Git Describe

git describe main

git describe side

git describe bugFix




### SEÇÃO: ADVANCED TOPICS


[1] Rebasing over 9000 times

git rebase main bugFix

git rebase bugFix side

git rebase side another

git rebase another main


[2] Multiple parents

git branch bugWork main~^2~


[3] Branch Spaghetti

git checkout one

git cherry-pick c4 c3 c2

git checkout two

git cherry-pick c5 c4 c3 c2

git branch -f three c2


## Remotes

### SEÇÃO: GIT REMOTES


[1] Clone Intro

git clone


[2] Remote Branches

git commit

git checkout o/main

git commit


[3] Git Fetchin'

git fetch


[4] Git Pullin'

git pull


[5] Faking Teamwork

git clone

git commit

git fakeTeamwork main 2

git pull


[6] Git Pushin'

git commit

git commit

git push



[7] Diverged History

git clone

git fakeTeamwork main

git commit

git pull --rebase

git push



[8] Locked Main

git reset o/main

git checkout -b feature c2

git push





### SEÇÃO: ADVANCED REMOTES


[1] Push Main!

git fetch

git rebase o/main side1

git rebase side1 side2

git rebase side2 side3

git rebase side3 main

git push


[2] Merging with remotes

git checkout main

git pull origin main

git merge side1

git merge side2

git merge side3

git push origin main


[3] Remote Tracking

git checkout -b side o/main

git commit

git pull --rebase

git push


[4] Git push arguments

git push origin main

git push origin foo


[5] Git push arguments expanded

git push origin main^:foo

git push origin foo:main


[6] Fetch arguments

git fetch origin c3:foo

git fetch origin c6:main

git checkout foo

git merge main


[7] Source of nothing

git push origin :foo

git fetch origin :bar


[8] Pull arguments

git pull origin c3:foo

git pull origin c2:side
