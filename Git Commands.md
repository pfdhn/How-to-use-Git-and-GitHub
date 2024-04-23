# Git Basic Commands

### Get git version
```
git -v
```

### Display all branches
```
git branch
```

### Create a branch
```
git branch BRANCH_NAME
```

### Go to a specific branch
```
git checkout BRANCH_NAME
```

### File Staging
To add a single file:
```
git add <filename>
```
To add all files for staging:
```
git add --all
```

### Commit changes to the branch
```
git commit -m '<this message >'
```
If you haven't added the edited files in the staging environment and invoked the commit command, you will be prompted to add the files first.
Below is an example of a commit where the long string is the SHA code or the unique id of the checkpoint created.

```
commit 719129f97170a103eee4d62cabbd37940a3a63f6
Author: pfdhn <email@gmail.com>
Date:   Tue Apr 16 22:11:29 2024 +0800

    Radio button fixed
```

### Create a branch from a commit
For example, you have already created 10 commits in a branch. Then you found out that along the way, the code was broken and the last time the code worked perfectly was on your 5th commit.
You may create a new branch from that checkpoint using the SHA code.
```
git branch NEW_BRANCH_NAME <SHA CODE>
```

### Check branch status
Make sure you checkout in the target branch using ```git checkout TARGET_BRANCH_NAME``` then use the following command to check branch status
```
git status
```

### Check logs
If you want to check the commits (or saved checkpoints) in a branch:
```
git log
```
You will see all the commits you made including the unique SHA code, author name, date committed, and message/note. Scroll down to see all commits and **press Q key to exit.** Below is an example output when ```git log``` is invoked.
```
commit 719129f97170a103eee4d62cabbd37940a3a63f6
Author: pfdhn <email@gmail.com>
Date:   Tue Apr 16 22:11:29 2024 +0800

    Radio button fixed

commit 0ae943d8815064187f9d4aee4da6d98e65ebd1dc
Author: pfdhn <email@gmail.com>
Date:   Tue Apr 16 15:02:56 2024 +0800

    Created a theme toggle feature

commit f356266e8c5cc463194397ab480997eeb898a45d
Author: pfdhn <email@gmail.com>
Date:   Tue Apr 16 10:19:25 2024 +0800

    Application draft
```

### Delete a branch
Delete a branch that has been pushed or merged with the main branch.
```
git branch -d  BRANCH_NAME
```
In some cases, we create a branch to do some experiment but will eventually not be merged to the main branch. To force delete a branch:
```
git branch -D  BRANCH_NAME
```
