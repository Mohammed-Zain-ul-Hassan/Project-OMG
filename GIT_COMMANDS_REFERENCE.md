# Git Commands Reference - Project OMG
**Software Construction & Development Task**  
**Student:** Mohammed Zain ul Hassan  
**Date:** October 3, 2025  
**Repository:** https://github.com/Mohammed-Zain-ul-Hassan/Project-OMG

---

## Task 1: Bootstrapping the Project

### Commands Executed:
```bash
git init
git config --global user.name "Mohammed Zain ul Hassan"
git config --global user.email "powehi29@gmail.com"
git add .
git commit -m "Initial commit: Bootstrap Project OMG with base code and documentation"
git remote add origin https://github.com/Mohammed-Zain-ul-Hassan/Project-OMG.git
git branch -M master
git push -u origin master
```

### Result:
- Repository initialized and pushed to GitHub
- **Commit ID:** 0bd901a
- **Files Added:** README.md, doc.txt, main.py, .gitignore

---

## Task 2: First Major Edit

### Commands Executed:
```bash
nano doc.txt  # Updated documentation with crucial details
git status
git diff doc.txt
git add doc.txt
git commit -m "Update documentation: Add crucial project details for launch preparation"
git push origin master
```

### Result:
- Documentation updated with key features and technical stack
- **Commit ID:** 4608537
- **Changes:** Added 19 lines, removed 3 lines

---

## Task 3: A New Feature in the Works

### Commands Executed:
```bash
git checkout -b b1
git branch
nano file2.txt  # Created revolutionary feature file
git status
git add file2.txt
git commit -m "Add revolutionary feature: Implement cloud interaction enhancement in file2.txt"
git push -u origin b1
```

### Result:
- Feature branch 'b1' created with file2.txt
- **Commit ID:** 551ae8a
- **Branch:** b1 (created and pushed to remote)
- **Files Added:** file2.txt (39 lines)

---

## Task 4: The Merge Challenge

### Commands Executed:
```bash
git checkout master
git branch
git pull origin master
git merge b1
git push origin master
```

### Result:
- Branch b1 successfully merged into master
- **Merge Type:** Fast-forward (no conflicts)
- **Files Added to Master:** file2.txt

---

## Task 5: Keeping the Codebase Clean

### Commands Executed:
```bash
git branch -d b1
git push origin --delete b1
git branch -a
```

### Result:
- Branch b1 deleted locally (was at commit 551ae8a)
- Branch b1 deleted from remote repository
- **Verification:** Only master branch remains

---

## Task 6: Marking a Milestone

### Part A - Creating Tag:
```bash
git tag -a v1.0 -m "Release v1.0: First stable milestone of Project OMG"
git tag
git push origin v1.0
```

### Result:
- Tag v1.0 created and pushed
- **Tag ID:** 1a9788b
- **Tagged Commit:** 551ae8a

### Part B - Removing Tag (CEO's Request):
```bash
git tag -d v1.0
git push origin --delete v1.0
git tag
git ls-remote --tags origin
```

### Result:
- Tag v1.0 removed locally and remotely
- **Verification:** No tags remain in repository

---

## Git Reflog Output (Complete Operation History)

```
551ae8a (HEAD -> master, origin/master, origin/HEAD) HEAD@{0}: merge b1: Fast-forward
4608537 HEAD@{1}: checkout: moving from b1 to master
551ae8a (HEAD -> master, origin/master, origin/HEAD) HEAD@{2}: commit: Add revolutionary feature: Implement cloud interaction enhancement in file2.txt
4608537 HEAD@{3}: checkout: moving from master to b1
4608537 HEAD@{4}: commit: Update documentation: Add crucial project details for launch preparation
0bd901a HEAD@{5}: Branch: renamed refs/heads/master to refs/heads/master
0bd901a HEAD@{7}: commit (initial): Initial commit: Bootstrap Project OMG with base code and documentation
```

### Reflog Analysis:
- **HEAD@{7}:** Initial repository setup
- **HEAD@{5}:** Branch renamed to master
- **HEAD@{4}:** Documentation updated on master
- **HEAD@{3}:** Switched to new branch b1
- **HEAD@{2}:** Revolutionary feature committed on b1
- **HEAD@{1}:** Switched back to master
- **HEAD@{0}:** Merged b1 into master (Fast-forward)

This reflog proves all branch operations were performed correctly, including the creation, use, and merge of branch b1.

---

## Final Repository State

### Commit History:
1. **0bd901a** - Initial commit: Bootstrap Project OMG with base code and documentation
2. **4608537** - Update documentation: Add crucial project details for launch preparation
3. **551ae8a** - Add revolutionary feature: Implement cloud interaction enhancement in file2.txt

### Branch Operations:
- ✅ Branch 'b1' was created from master
- ✅ Feature developed in isolation on b1
- ✅ Successfully merged b1 → master (fast-forward)
- ✅ Branch b1 deleted after merge (local and remote)

### Tag Operations:
- ✅ Tag 'v1.0' created on commit 551ae8a
- ✅ Tag 'v1.0' deleted upon CEO's request (local and remote)

### Current State:
- ✅ All files committed and pushed to master
- ✅ Documentation updated with crucial details
- ✅ Revolutionary feature (file2.txt) merged into master
- ✅ Clean commit history maintained
- ✅ Only master branch exists (locally and remotely)
- ✅ No tags exist (locally and remotely)
- ✅ No untracked or uncommitted files

---

## Command Explanations

### Flags Used:
- **`-m`**: Add commit/tag message inline
- **`-u`**: Set upstream tracking for push
- **`-b`**: Create new branch and switch to it
- **`-d`**: Delete branch/tag (safe delete)
- **`-a`**: Create annotated tag (with metadata)
- **`-M`**: Force rename/move branch

### Key Commands:
- **`git init`**: Initialize new Git repository
- **`git add .`**: Stage all files in current directory
- **`git commit`**: Create snapshot of staged changes
- **`git push`**: Upload commits to remote repository
- **`git checkout -b`**: Create and switch to new branch
- **`git merge`**: Integrate changes from another branch
- **`git tag`**: Create reference point for specific commit
- **`git reflog`**: Show complete history of HEAD movements

---

## Evidence of Completed Tasks

### Task Completion Checklist:
- ✅ **Task 1:** Repository initialized, files committed, and pushed to GitHub
- ✅ **Task 2:** Documentation updated with urgent details and pushed
- ✅ **Task 3:** Feature branch b1 created, file2.txt added, and pushed
- ✅ **Task 4:** Branch b1 merged into master successfully (no conflicts)
- ✅ **Task 5:** Branch b1 cleaned up (deleted locally and remotely)
- ✅ **Task 6:** Tag v1.0 created and subsequently removed as requested

### Proof Sources:
1. **Commit messages** clearly describe each task
2. **Git reflog** shows all branch operations
3. **file2.txt content** documents it was developed on branch b1
4. **GitHub repository** shows clean final state with all work merged
5. **This reference document** provides complete command history

---

## Notes

This document serves as a complete record of all Git operations performed during the Project OMG setup. All tasks were completed as per requirements, demonstrating proficiency in:

- Repository initialization and remote configuration
- File staging, committing, and pushing
- Branch creation, switching, and management
- Merging branches (conflict-free fast-forward merge)
- Branch cleanup (local and remote deletion)
- Tag creation and removal
- Clean commit history maintenance
- Professional Git workflow practices

---

**Repository URL:** https://github.com/Mohammed-Zain-ul-Hassan/Project-OMG  
**Submitted by:** Mohammed Zain ul Hassan  
**Course:** Software Construction & Development  
**Institution:** Emumba
