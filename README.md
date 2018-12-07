# AABMM
## Setting up AABMM on your Mac for the first time
1. Make sure you have [XAMPP](https://www.apachefriends.org) (Mac), installed.
2. Open the terminal app
3. run (paste into terminal and press enter) `cd / && cd Applications/XAMPP/htdocs && mkdir AABMM && cd AABMM` This will navigate to your local server, make a folder for AABMM, and then go into that folder.
4. run `git init`
5. run `git remote add origin https://github.com/AABMM/AABMM.git`
6. run `git pull origin master`
7. run `ls` you should see a bunch of files and folders. 
8. Open the XAMPP app and go to MANAGE SERVERS. Start all of the servers.
9. Open your web browser and go to `http://localhost/phpmyadmin`
10. Go to the Users tab and click ADD USER. The host should be set to `localhost`. Check `Create database with same name and grant all privileges`. Write down your username and password. 
11. In your browser, go to `http://localhost/AABMM` and follow the setup instructions. 

## Making changes safely (even in the admin panel)
1. Open the terminal app and run `cd / && cd Applications/XAMPP/htdocs/AABMM`
2. run `git branch`. You will see a star next to your current branch. 
3. run `git checkout -b BRANCHNAME` to make a new branch or `git checkout BRANCHNAME` to use an existing branch. Dont use the master branch.
4. Make all of your changes. 
5. run `git status` to see if any files or folders were changed. If not, you can stop here.
6. run `git commit -a -m "description of the change that you made"`. Your change is now saved on your computer.
7. run `git push origin BRANCHNAME`. Your change is now saved on github. 
8. If you are done making changes, go to https://github.com/AABMM/AABMM/tree/BRANCHNAME and click `create pull request`. It will check if its safe to merge that code with the master branch, and if so, allow you to merge.

TIP: Keep your commits small. You should be able to describe each one in a sentence or two. Here is an example of some appropreate commits

NEW BRANCH: contact-page

Commit 1: "Build contact page layout"

Commit 2: "Build contact page form"

Commit 3: "Add contact page location, phone number, and map"

Commit 4: "Style contact page"

Commit 5: "Clean up"

PUSH contact-page to origin contact-page

Create pull request
