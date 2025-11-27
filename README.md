# GitHub_tutorial
"Forgot Git again? 😂 Don’t worry — let me help you relearn it 🔁"

HERE WE WILL UNDERSTAND ALL THE IMPORTANT COMMANDS THAT ARE REQUIRED TO USE GIT HUB AND GIT .
<br>
Start with the introduction.
Git is a version control tool/software that keeps a track of the changes also known as "commits" . 
These projects/code is pushed in the form of folders called repository.

GitHub - It is a website that is required to manage and store the code on cloud. Also known as remote.

Commands -->
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

These commands is like identifiers of the commits that an author will do and just helps to keep an information of the author who tries to do the commit.

Basic git commands:

git clone <link>   ---> Clones the github repository(project) to the local machine.
git status    --> gives the status of the local with respect to the remote/github .




Init Commands 

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
This origin is just a name of the remote repo.







