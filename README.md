# GitHub_tutorial
"Forgot Git again? 😂 Don’t worry — let me help you relearn it 🔁"

HERE WE WILL UNDERSTAND ALL THE IMPORTANT COMMANDS THAT ARE REQUIRED TO USE GIT HUB AND GIT .
<br>
Start with the introduction.
Git is a version control tool/software that keeps a track of the changes also known as "commits" . 
These projects/code is pushed in the form of folders called repository.

GitHub - It is a website that is required to manage and store the code on cloud. Also known as remote.

1. SETUP AND CONFIGURATION ⚙️
<br>
pwd --> Helps to know the present working directory.
<br>
Configuration steps on Git.
git config --global user.name "User name"
<br>
git config --global user.email "example@gmail.com"
<br>
git config --list ----> Gives the complete details of configuration done on the git bash till now.
<br>
👉 Before anything else, Git must know who you are.
<br>

These commands is like identifiers of the commits that an author will do and just helps to keep an information of the author who tries to do the commit.

2. Creating / Initializing a Repo 🆕
<br>
git init This command is used to turn a normal folder into git repository by creating a .git file)
<br>
Create  a repo in the github and using url we can push our folder on github.
<br>
git remote add origin <link> (tells the git which remote repo we will push the changes to.)
<br>
git remote -v (verify remote)
<br>
git branch (to check branch of github)
<br>
git branch -M main (modify the branch name to main by default it is master)
<br>
git push -u origin main (-u sets the upstream brach to origin/main) this command will set the upstream so all the changes will be pushed to origin/main
<br>
NOTES ----> This origin is just a name of the remote repo.
<br>
👉 This is local → remote.
<br>

3. CLONING AND WORKING WITH REMOTE 🧰

git clone <link>   ---> Clones the github repository(project) to the local machine.
git status    --> gives the status of the local with respect to the remote/github .

👉 This is remote → local.
<br>

4. Branching 🌿
<br>
git branch ---> (Checks the branches on the repo.)
<br>
git checkout <--branchname> (Switches to the branch)
<br>
git checkout -b <--branchname> (Creates a new branch)
<br>
git switch <--branchname> (almost similar to git checkout but used only for branches , and not checkout files or anything)
<br>
git switch -c <--branchname> (create new branch)
<br>
👉 Before merge, branches should come first.
<br>

5. Merging 🔀
<br>
by command line we can do it like.
<br>
check if there is any conflict between the branches and resolve it if any.
<br>
git diff <--other branch-->
<br>
If there is any difference you can use the editor to resolve it and you can decide manually which changes you want to keep.
<br>
Then we can merge the current branch to the required branch(like main) 
<br>
git merge <--other branch  name>
<br>

Way 2 to merge two branches. --> Use pull request and fetch the changes on the remote branch and then merge request is generated to merge with the other branch.
<br>
👉 Logical continuation after branching.
<br>

6. UNDOING AND FIXING MISTAKES ↩️
   <br>

CASE 1 : staged changes(add)
<br>
git reset <--filename-->  if you have done changes in one file.
<br>
git reset   (for multiple file changes)
<br>
CASE 2 : commit changes.
<br> 
For reverting to just previous commit.
<br>
git reset HEAD ~1
<br>
For reverting multiple commits you need to get the hash of the commit you want to revert to .
<br>
git log (helps to fetch the history of commits.)
<br>
git reset --hard <commit-hash> (this commit hash can be pasted from the git log details, --hard is used to view that reset in the vs code if you are using it else you can remove it.)
<br>
👉 This should come after commit, branch, and merge.
<br>

7. SSH Setup (Optional for advanced users) 🔑

   GitHub provides an authentication using ssh key as well so that later we can clone and use the repository. For that a ssh key needs to be generated that contains two keys,
   private(saved in local machine) and public(uploaded on github). These keys are used for authentication everytime we use the repo.
   <br>
   ssh-keygen -t ed25519 -C "example@gmail.com" (generates ssh key can be run on powershell and cmd, but git bash preferred)
   <br>
   cat ~/.ssh/id_ed25519.pub (to view the public key on the terminal)
   <br>
   git remote set-url origin <---ssh link---> (set the origin/repo for push and pull operation)
   <br>
   👉 This comes last because it's advanced configuration.







