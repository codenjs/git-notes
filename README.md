**Create New Branch with Current Changes**  
then commit in the new branch and switch back to master

`git checkout -b topic/newbranch`

- https://stackoverflow.com/questions/3899627/create-git-branch-with-current-changes
- https://stackoverflow.com/questions/1453129/git-create-branch-from-current-checked-out-master

---
**Copy branch to master without merging or making a "merge" commit**  
then do more work before committing to master

`git merge --squash branchA`

- https://stackoverflow.com/questions/9599411/differences-between-git-merge-squash-and-no-commit
- https://stackoverflow.com/questions/20045946/applying-the-changes-from-branch-b-to-a-without-merging-or-adding-commits

---
**Copy existing branch to new branch and squash**  
then check in as one commit, or diff with master

// assuming you're already on old_branch  
`git checkout -b new_branch`  
// squash the last 3 commits  
`git rebase -i HEAD~3`

- https://stackoverflow.com/questions/14998923/how-can-i-copy-the-content-of-a-branch-to-a-new-local-branch
- https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git
- https://blog.carbonfive.com/2017/08/28/always-squash-and-rebase-your-git-commits/

---
**Merge specific files from another branch**

`git checkout source_branch <paths>...`  

- https://stackoverflow.com/questions/449541/how-to-selectively-merge-or-pick-changes-from-another-branch-in-git
- https://jasonrudolph.com/blog/2009/02/25/git-tip-how-to-merge-specific-files-from-another-branch/

---
**Merge a branch, solving all conflicts by keeping changes from the branch**

`git merge --no-commit -X theirs somebranch`

- https://stackoverflow.com/questions/14275856/merging-but-overwriting-changes-in-git
- https://stackoverflow.com/questions/173919/is-there-a-theirs-version-of-git-merge-s-ours

---
**Get latest from master into current branch**  
possibly rebase or merge?

`git checkout current_branch`  
`git rebase master`

- https://stackoverflow.com/questions/804115/when-do-you-use-git-rebase-instead-of-git-merge

---
**Compare file between branches**

`git diff master -- "C:\path\file.cs"`

- https://stackoverflow.com/questions/9113280/diff-current-working-copy-of-a-file-with-another-branchs-committed-copy

---
**Change file in prior commit**

`git rebase --interactive 'bbc643cd^'`  
`git commit --all --amend --no-edit`  
`git rebase --continue`

- https://stackoverflow.com/questions/1186535/how-to-modify-a-specified-commit

---
**Change prior commit message**

// change last commit  
`git commit -m "corrected message" --amend`  
// change second last commit  
`git rebase -i HEAD~2`

- https://stackoverflow.com/questions/45391201/change-unpushed-previous-git-commit-message

---
**Change prior commit date**

`git commit --amend --date="Fri Feb 1 22:39:25 2019 -0500"`

- https://stackoverflow.com/questions/454734/how-can-one-change-the-timestamp-of-an-old-commit-in-git

---
**Undo a commit**

// this left the commit in the history, but I updated the files and re-committed with the same message  
`git reset HEAD~1`  
`git reset --soft HEAD~1`

- https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git

---
**Undo a merge**

`git reset --hard HEAD~1`

- https://stackoverflow.com/questions/2389361/undo-a-git-merge-that-hasnt-been-pushed-yet

---
**Undo a rebase**

// find the actions to undo  
`git reflog`  
`git reset --hard "HEAD@{5}"`

- https://stackoverflow.com/questions/134882/undoing-a-git-rebase

---
**Delete Local Branch**

`git branch -d branch_name`

- https://stackoverflow.com/questions/2003505/how-do-i-delete-a-git-branch-both-locally-and-remotely

---
**Recreate a branch after it was deleted**

`git checkout -b <branch> <sha>`

- https://stackoverflow.com/questions/3640764/can-i-recover-a-branch-after-its-deletion-in-git

---
**Pull Requests**
- https://ardalis.com/github-pull-request-checklist
- https://www.digitalocean.com/community/tutorials/how-to-create-a-pull-request-on-github
- https://git-scm.com/book/en/v2/GitHub-Contributing-to-a-Project
