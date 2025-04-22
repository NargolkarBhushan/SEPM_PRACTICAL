# SEPM_PRACTICAL

Aim 1: Clone, Create, Commit, and Push to Remote
git clone https://github.com/username/repository-name.git
cd repository-name

git checkout -b feature-branch
echo "This is a new file added in feature-branch." > newfile.txt
git add newfile.txt
git commit -m "Add newfile.txt with initial content"
git push origin feature-branch

Aim 2: Create and Merge Branches
git clone https://github.com/username/repository-name.git
cd repository-name
git checkout -b my-feature
echo "Added a new line in my-feature branch." >> README.md
git add README.md
git commit -m "Update README.md with a new line in my-feature branch"
git checkout main
git merge my-feature
git log --oneline --graph --all


Aim 3: Revert a Commit
git clone https://github.com/username/repository-name.git
cd repository-name

echo "Line 1" > file.txt
git add file.txt
git commit -m "Add line 1"

echo "Line 2" >> file.txt
git add file.txt
git commit -m "Add line 2"

echo "Line 3" >> file.txt
git add file.txt
git commit -m "Add line 3"

git log --oneline  # Find the commit hash to revert (e.g., abc123)
git revert abc123  # Replace abc123 with the actual commit hash of "Add line 2"
git log --oneline  # Verify the revert commit

Aim 4: Modify a Commit Message (Amend Last Commit)
git clone https://github.com/username/repository-name.git
cd repository-name

echo "Initial commit content" > file.txt
git add file.txt
git commit -m "Initial commit message"

git commit --amend -m "Updated commit message"
git log --oneline  # Verify amended message


🔹 Aim 5: Stash, Apply, and Pop Changes
git clone https://github.com/username/repository-name.git
cd repository-name

echo "Uncommitted changes" >> README.md
git stash

git checkout -b temp-branch
git checkout main  # Or original branch

git stash apply  # OR use: git stash pop

git add README.md
git commit -m "Apply stashed changes to README.md"

