# Using Git and GitHub with RStudio
Lets begin by opening a new **RStudio Project**. To do this click **File > New Project > New Directory > Empty Project**

![img6](http://www.datasurg.net/wp-content/uploads/2015/07/7_new_project.jpg)

![img7](http://www.datasurg.net/wp-content/uploads/2015/07/8_new_project_with_git.jpg)

Lets give your project the name **Test** and set the location to your **Desktop** folder.  
> Also please be sure to click the optional **Create a git repository** option!!!

This will start a new clean RStudio session. Note if you have done this properly then two files will be placed in your new directory/folder named Test (you can see these in your Files pane of RStudio interface). We will talk more about these later. If you dont see these files then please let me know.

## Create some new content that we will track with Git and add to GitHub.
In RStudio, click **File -> New File > *R Markdown document > From Template > GitHub Document > OK**.
This will create a new document in your project. Save this with the name **RStudio_report**. 

> Note dont use spaces in your files names please - unix systems dont like this.

Now in RStudio a black-red-green GIT icon on the top toolbar. Click this and then **Git > Commit...**
This should bring up a new window where we can "Stage" or Add our files and for version control tracking and provide a descriptive commit message.  

Stop here for a demo from Barry if you like.

Control, select Git.



## Setup Git within RStudio and associate with GitHub
In RStudio, click **Tools -> Version Control, select Git.

![img1](http://www.datasurg.net/wp-content/uploads/2015/07/1.jpg)
 
In RStudio, Tools -> Global Options, select Git//SVN tab. Ensure the path to the Git executable is correct. This is particularly important in Windows where it may not default correctly (e.g. C:/Program Files (x86)/Git/bin/git.exe).

Now hit, Create RSA Key …

![img2](http://www.datasurg.net/wp-content/uploads/2015/07/2_rsa.jpg)

Close this window.

Click, View public key, and copy the displayed public key.

![img3](http://www.datasurg.net/wp-content/uploads/2015/07/4_rsa.jpg)

If you haven’t already, create a GitHub account. Open your account settings and click the SSH keys tab. Click Add SSH key. Paste in the public key you have copied from RStudio.

Tell Git who you are. Remember Git is a piece of software running on your own computer. This is distinct to GitHub, which is the repository website. In RStudio, click Tools -> Shell … . Enter:

	git config --global user.email "mail@ewenharrison.com" 
	git config --global user.name "ewenharrison"

Use your GitHub username.

![img5](http://www.datasurg.net/wp-content/uploads/2015/04/10_who_are_you.jpg)

## CREATE NEW PROJECT AND GITHUB REPO

In RStudio, click New project as normal. Click New Directory.

Open a new **R Markdown** document > From Template > GitHub Document.

![img6](http://www.datasurg.net/wp-content/uploads/2015/07/7_new_project.jpg)

Now you want to push the contents of this commit to GitHub, so it is also backed-up off site and available to collaborators. 
In GitHub, create a New repository by clicking the plus **+** in the top nav bar here and then **New repository**. I named mine “test”.

![img7](http://www.datasurg.net/wp-content/uploads/2015/07/8_new_project_with_git.jpg)

![img8](http://www.datasurg.net/wp-content/uploads/2015/07/5_create_git.jpg)

## Add the repo to RStudio
On the resulting GitHub web page copy the text under _”…or push an existing repository from the command line”_.  We will need to add this to our RStudio project.

Then in RStudio, again click Tools -> Shell … . Enter:

And then paste your copyed code in to the shell. Mine looked something like this:

	git remote add origin https://github.com/bioboot/test.git 
	git config remote.origin.url git@github.com:bioboot/test.git 
	git push -u origin master
	
After saving your new script (test.R), it should appear in the Git tab on the Environment / history panel.

![img9](http://www.datasurg.net/wp-content/uploads/2015/07/13_push_pull.jpg)

You have now pushed your commit to GitHub, and should be able to see your files in your GitHub account. The Pull Push buttons in RStudio will now also work. Remember, after each Commit, you have to Push to GitHub, this doesn’t happen automatically.

