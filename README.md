# GIT-PRACTICE



Day-2 Git Safe Push Workflow Cheat Sheet

🔹 Goal: Learn to commit, push, and manage Git safely without errors or secrets, step by step.

1️⃣ Setup & Check Repository

✅ Step 1: Open your Git terminal / PowerShell

✅ Step 2: Navigate to your project folder

cd "C:\Users\dell\OneDrive\Desktop\GIT practice"


✅ Step 3: Check the current branch & status

git status
git branch


Explanation:

git status → shows files changed, staged, untracked

git branch → shows current branch

2️⃣ Stage Changes

✅ Step 4: Add files safely (without secrets)

git add <filename>        # add specific file
git add .                 # add all files in folder


Explanation:

Staging means marking files ready for commit

Always double-check files before staging

3️⃣ Commit Changes

✅ Step 5: Commit with a message

git commit -m "Add descriptive message"


Example:

git commit -m "Add DevOps Diary entry without secrets"


Explanation:

-m → your commit message

Avoid secrets in commit messages

✅ Tip: If you forgot to add a file:

git add <file>
git commit --amend --no-edit


Adds file to last commit without changing message

4️⃣ Pull Remote Changes (Avoid Non-Fast-Forward)

✅ Step 6: Always pull before pushing

git pull origin master --rebase


Explanation:

Updates your branch with remote changes

--rebase keeps history clean

Resolve conflicts if prompted, then:

git add <resolved-file>
git rebase --continue

5️⃣ Push Changes to Remote

✅ Step 7: Push to GitHub

git push -u origin master


✅ If you rewrote history (removed secret commits):

git push -u origin master --force


Explanation:

Push sends commits to GitHub

Force push only after cleaning history

6️⃣ Verify Commit & No Secrets

✅ Step 8: Check logs

git log --oneline
git log -p


✅ Step 9: Search for secrets

git log -p | findstr "token"


✅ Step 10: Check files on GitHub web

7️⃣ General Safety Tips

Never commit tokens, passwords, or sensitive info

Use .gitignore for files with secrets

Stage and commit frequently to avoid large risky commits

Always pull before push to avoid conflicts
