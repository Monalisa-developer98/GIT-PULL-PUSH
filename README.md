"# GIT-PULL-PUSH" 
Git Push through Command Line 
Steps:

Step:1
 echo “#reponame” >> README.md
 git init
 git add README.md 


Step:2
	git commit -m “first commit” 
	git branch -M main
	git remote add origin “path repo”
	git push -u origin main
	


Lets take an example -
echo "# MOMFrontend" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SAHOOPRATISHRUTI/MOMFrontend.git
git push -u origin main

Git Pull through Command Line 
Steps:

Step:1
	Fork the Repository
Step:2
	git clone “path of the clone repo”
Step:3
	Create a new branch and Switch to it — git checkout -b ‘branch-name’
Step:4
	git remote add Upstream(when you changes anything in the clone project  the changes also          syncing to the origin project )  —-- git remote add upstream “original-repo-path”

Step:5
	Change and Update what do you want to do
Step:6
	Verify the changes you made —- git diff –word-diff
Step:7
	Commit your Changes to the branch  —-  git commit -a -m “ commit-by-XXXX”
Step:8
	Push the branch backup to your git hub repo – git push origin ‘branch name’



 https://docs.google.com/document/d/1cwj54bsI3q_MwhxqFzBxOG9qqW8ZRYcn5MOlW4Raz6o/edit?usp=sharing---acess this link  for the worf file

=================================================================================================
**Repository Permissions:**
----------------------------
git config --global user.name   -------- git config --global user.name "Monalisa-developer98"
git config --global user.email    ------ git config --global user.email "your-email@example.com"

**Step 1:** Check for an Existing SSH Key
First, check if you already have an SSH key set up on your system:

bash
ls -al ~/.ssh
If you see files like id_rsa and id_rsa.pub, then you likely already have an SSH key. If not, you’ll need to generate one.

**Step 2:** Generate a New SSH Key (If Needed)
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"

	When prompted, save the key to the default location (/home/username/.ssh/id_rsa) by pressing Enter.
	Choose a passphrase or leave it empty for no passphrase.

**Step 3:** Add Your SSH Key to the SSH Agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa

**Step 4:** Add the SSH Key to Your GitHub Account
cat ~/.ssh/id_rsa.pub

	Go to GitHub:
 	------------------
	Navigate to Settings > SSH and GPG keys.
	Click on New SSH key.
	Give it a title (e.g., "My Laptop") and paste the SSH key you copied.
	Click Add SSH key.

 **Step 5:** Test Your SSH Connection to GitHub
 ssh -T git@github.com

If your SSH key is set up correctly, you should see a message like: Hi Monalisa-developer98! You've successfully authenticated,

**Step 6:** Set Your Remote to Use SSH
git remote -v
git remote set-url origin git@github.com:Monalisa-developer98/MERN-Stack-Crud-App.git

**Step 7:** Push Changes
git push -u origin main



edit by Monalisa------------------pratishruti
