# GitHub_tutorial
"Forgot Git again? 😂 Don’t worry — let me help you relearn it 🔁"
<br><br>

HERE WE WILL UNDERSTAND ALL THE IMPORTANT COMMANDS THAT ARE REQUIRED TO USE GITHUB AND GIT.
<br><br>

Start with the introduction.
<br>
Git is a version control tool/software that keeps a track of the changes also known as "commits".
These projects/code is pushed in the form of folders called repository.
<br><br>

GitHub - It is a website that is required to manage and store the code on cloud. Also known as remote.
<br><br>

1. SETUP AND CONFIGURATION ⚙️
<br><br>

pwd --> Helps to know the present working directory.
<br>
Configuration steps on Git:
<br>
git config --global user.name "User name"
<br>
git config --global user.email "example@gmail.com"
<br>
git config --list ----> Gives the complete details of configuration done on the git bash till now.
<br><br>

👉 Before anything else, Git must know who you are.
<br>
These commands act like identifiers of commits to help keep information of the author.
<br><br>

2. Creating / Initializing a Repo 🆕
<br><br>

git init --> Turns a normal folder into a git repository by creating a .git folder.
<br>
Create a repo on GitHub and use its URL to push the local folder to GitHub.
<br>
git remote add origin <link> --> Tells git which remote repo we will push the changes to.
<br>
git remote -v --> Verify remote.
<br>
git branch --> Check current branch.
<br>
git branch -M main --> Modify branch name to main (default is master).
<br>
git push -u origin main --> (-u sets the upstream branch to origin/main) so all changes will be pushed there.
<br>
NOTES ----> "origin" is just a name of the remote repo.
<br><br>

👉 This is local → remote.
<br><br>

3. CLONING AND WORKING WITH REMOTE 🧰
<br><br>

git clone <link> --> Clones the GitHub repository (project) to the local machine.
<br>
git status --> Gives the status of the local repo with respect to GitHub/remote.
<br><br>

👉 This is remote → local.
<br><br>

4. Branching 🌿
<br><br>

git branch --> Check branches.
<br>
git checkout <branchname> --> Switches to the branch.
<br>
git checkout -b <branchname> --> Creates a new branch and switches to it.
<br>
git switch <branchname> --> Similar to checkout but used only for switching between branches.
<br>
git switch -c <branchname> --> Creates and switches to new branch.
<br><br>

👉 Before merge, branches should come first.
<br><br>

5. Merging 🔀
<br><br>

By command line:
<br>
Check if there is any conflict between branches and resolve it.
<br>
git diff <other-branch>
<br>
If there is any difference, use the editor to resolve conflicts manually.
<br>
git merge <other-branch> --> Merge current branch with the other branch (like main).
<br><br>

Way 2:
<br>
Use Pull Request on GitHub → Fetch the changes → Create merge request → Merge into the target branch.
<br><br>

👉 Logical continuation after branching.
<br><br>

6. UNDOING AND FIXING MISTAKES ↩️
<br><br>

CASE 1: Staged changes (after git add)
<br>
git reset <filename> --> Unstage one file.
<br>
git reset --> Unstage all files.
<br><br>

CASE 2: Commit changes
<br>
git reset HEAD~1 --> Revert to previous commit.
<br>
git log --> Fetch the history of commits.
<br>
git reset --hard <commit-hash> --> Reset to a specific commit (hash from git log). --hard shows the reset in your editor like VS Code.
<br><br>

👉 This should come after commit, branch, and merge.
<br><br>

7. SSH Setup (Optional for advanced users) 🔑
<br><br>

GitHub provides authentication using SSH keys.  
SSH keys include a private key (local machine) and a public key (uploaded on GitHub).
These are used for password-less authentication for cloning, pushing, and pulling.
<br><br>

ssh-keygen -t ed25519 -C "example@gmail.com" --> Generates SSH key (Git Bash recommended).
<br>
cat ~/.ssh/id_ed25519.pub --> View the public key on terminal.
<br>
git remote set-url origin <ssh-link> --> Set origin remote to SSH-based link.
<br><br>

👉 This comes last because it's advanced configuration.
