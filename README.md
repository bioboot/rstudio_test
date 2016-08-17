# rstudio_test
This is a set of instructions for class  

## Setup Git within RStudio and associate with GitHub
In RStudio, Tools -> Version Control, select Git.

 

In RStudio, Tools -> Global Options, select Git//SVN tab. Ensure the path to the Git executable is correct. This is particularly important in Windows where it may not default correctly (e.g. C:/Program Files (x86)/Git/bin/git.exe).

Now hit, Create RSA Key …

Close this window.

Click, View public key, and copy the displayed public key.

If you haven’t already, create a GitHub account. Open your account settings and click the SSH keys tab. Click Add SSH key. Paste in the public key you have copied from RStudio.

Tell Git who you are. Remember Git is a piece of software running on your own computer. This is distinct to GitHub, which is the repository website. In RStudio, click Tools -> Shell … . Enter:

	git config --global user.email "mail@ewenharrison.com" 
	git config --global user.name "ewenharrison"

Use your GitHub username.

## CREATE NEW PROJECT AND GITHUB REPO

In RStudio, click New project as normal. Click New Directory.

Open a new **R Markdown** document > From Template > GitHub Document.

Now you want to push the contents of this commit to GitHub, so it is also backed-up off site and available to collaborators. In GitHub, create a New repository, called here test.

 Click the + here and new repository. I named mine “rstudio_test”

## Add the repo to RStudio
Copy the text under _”…or push an existing repository from the command line”_ displayed on the GitHub page. We will need to add this to our RStudio project.

Then in RStudio, again click Tools -> Shell … . Enter:

And then paste your copyed code in to the shell.

You have now pushed your commit to GitHub, and should be able to see your files in your GitHub account. The Pull Push buttons in RStudio will now also work. Remember, after each Commit, you have to Push to GitHub, this doesn’t happen automatically.

