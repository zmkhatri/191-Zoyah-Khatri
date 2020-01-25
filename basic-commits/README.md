# Git Kata: Basic Commits
This kata will introduce you to the `git add` and `git commit` commands.

This is a very introductory kata. if you have used `git status`, `git log --oneline --graph`, `git add` and `git commit` extensively you should probably skip it.

You can look at the bottom of this file, if you have not yet done basic git configuration.

## Setup:

1. Run `. setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

1. Use `git status` to see which branch you are on.
2. What does `git log` look like?
    On branch master
    Your branch is up to date with 'origin/master'.

    nothing to commit, working tree clean
3. Create a file
4. What does the output from `git status` look like now?
    On branch master
    Your branch is up to date with 'origin/master'.

    Untracked files:
    (use "git add <file>..." to include in what will be committed)

        newFile.txt

5. `add` the file to the staging area
6. How does `git status` look now?
    On branch master
    Your branch is up to date with 'origin/master'.

    Changes to be committed:
    (use "git reset HEAD <file>..." to unstage)

        new file:   newFile.txt
7. `commit` the file to the repository
8. How does `git status` look now?
    On branch master
    Your branch is ahead of 'origin/master' by 1 commit.
    (use "git push" to publish your local commits)

    nothing to commit, working tree clean
9. Change the content of the file you created earlier
10. What does `git status` look like now?
    On branch master
    Your branch is ahead of 'origin/master' by 1 commit.
    (use "git push" to publish your local commits)

    nothing to commit, working tree clean
    dhcp-v124-018:basic-commits zoyah$ git status
    On branch master
    Your branch is ahead of 'origin/master' by 1 commit.
    (use "git push" to publish your local commits)

    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   newFile.txt

    no changes added to commit (use "git add" and/or "git commit -a")
11. `add` the file change
12. What does `git status` look like now?
    On branch master
    Your branch is ahead of 'origin/master' by 1 commit.
     (use "git push" to publish your local commits)

    Changes to be committed:
    (use "git reset HEAD <file>..." to unstage)

        modified:   newFile.txt
13. Change the file again
14. Make a `commit`
15. What does the `status` look like now? The `log`?
    status:
        On branch master
        Your branch is ahead of 'origin/master' by 2 commits.
        (use "git push" to publish your local commits)

        nothing to commit, working tree clean
    log:
        commit daca5fb6d23a47db9609d0c354cd44671121c8dc (HEAD -> master)
        Author: Zoyah Mariam Khatri <zkhatri@uci.edu>
        Date:   Fri Jan 24 18:28:14 2020 -0800

        second commit

        commit 2eba3ecaf8f5df1d32f67b149df36d9edca82f95
        Author: Zoyah Mariam Khatri <zkhatri@uci.edu>
        Date:   Fri Jan 24 18:25:38 2020 -0800
16. Commit the newest change

## Useful commands
- `git add`
- `git commit`
- `git commit -m "My commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `touch filename` to create a file (or `sc filename ''` in PowerShell)
- `echo content > file` to overwrite file with content (or `sc filename 'content'` in PowerShell)
- `echo content >> file` to append file with content (or `ac filename 'content'` in PowerShell)


## Git Initial Configuration
1. `git config --global user.name "John Doe"`
1. `git config --global user.email "johndoe@example.com`

For the vim scared:
- `git config --global core.editor nano`

For the windows peeps:
- `git config --global core.editor notepad`

Other editor options:
- `git config --global core.editor "atom --wait"`
- `git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst"`
