- Check if Git is installed on your computer
	- `git --version`

# Repositories
## GitHub
- What's the difference between Git and GitHub?
	- Git is the tool that allows software engineers to track changes
	- GitHub is the website that hosts Git repositories
	- You can use Git without GitHub, but you cannot use GitHub without Git
- Code is stored in **repositories** (repos) on GitHub, which are like folders for your code files and resources
##  Git Commands
## Using Git
- You have a repository on GitHub
- Now we will push our code to the **remote repository**
- It's empty right now, so let's work on adding some code
## Git Init
- `git init` initializes a new Git repository
- First command you run when you have a new project and want to **start tracking changes**
- When you run this command, Git will create a new directory named .git in your project folder
	- This directory contains all the information about your project's history and configuration
	- The terminal will output the following once completed successfully:
		- `Initialized empty Git repository in /Users/username/.git`
## Git Remote
- Now we need to connect our local repository (folder on computer) with our remote repository (the link on GitHub)
- We can use `remote add` to connect our local and remote repositories
	- `git remote add origin <repository_url>`
## Git Branch
- Let's rename the branch to `main`
- This will be the branch we *push code to* and will be default branch
	- `git branch -M main`
## Instructions
- Navigate to your project folder or directory on your computer
	- This can be any .py, .html, .css, .js file
- Open your selected folder in a code editor of your choice
- Open a terminal or command prompt
	- In VS Code, you can open the terminal with `CTRL + '`' or go to Terminal > New Terminal
- Once here, we're ready to connect our code on our device to our GitHub repo
- Before we begin, we want to make sure that your terminal is in the correct place to initialize the repository
	- `pwd`
- Next, create a connection between the file in our machine and the GitHub repo by linking them with the `git init`, `git remote add`, and `git branch` commands
- To check we have successfully connected our local and remote repositories and renamed the branch, run the following command:
```
git branch
// Output:
// * main
```
- If you see `main` in the output you're all set

# Git Workflow
## Working Directory
- The **working directory** is where you have the files and folders on your computer that you're actively working on or changing
- When you make changes to your files, Git will track these changes and allow you to move them to the staging area
## Staging Area / Index
- The **staging area** is a status of files and folders within your project that tells Git "Hey, I'm getting ready to go online"
- Temporary area where you pick and choose what files you want to "commit" or send to the remote repository
- Using the `git add` command allows us to do so; variation examples:
	- `git add example.txt` will add the single file to the staging area
		- If you only want one of your working files to show up on GitHub rather than the rest of your project, consider specifying a specific file
	- `git add .` will add **all** the changed files to the staging area
		- This means that any new file added or changed to the working directory will be included
	- `git add *.html` will only stage files with a specified extension
		- In this example, this command will only add **.html** files
## Committed Files
- Committing files are about sharing the current code as a "snapshot" that GitHub online has access to
- Commits help us separate different actions in our code, and allow us to add helpful messages so we know and keep track of changes
- Typical project commit examples:
	- `initial commit` - our first commit
	- `add fun pics to header` - developer added a header to their project
	- `fixed again fr this time!!!` - developer fixed a bug
- **Note**: commit messages get silly when you're working on your own for a while, but short, clear, and descriptive messages are needed when working on a team
- We want messages to explain what we're doing to the code so other devs can know what was worked on at a glance
- Commit your staged files:
	- `git commit -m 'Your commit message here!'`
## Instructions
- Go back to your terminal or command prompt, and navigate to your project folder
- Use `git add .` to commit all the files in your project folder to the staging area
- Then use `git commit -m 'Initial Commit'` to write your first commit message

# Local Push
## Git Status
- The `git status` command is used to check the status of your files
- It is a handy command that will show you which files are staged, unstaged, and untracked
	- **Staged** files are ready to be committed
	- **Unstaged** files are not yet ready to be committed
	- **Untracked** files are new files that Git has not seen before
- Check the status of your files: 
	- `git status`
## Git Push
- The `git push` command is used to send your locally committed changes to your remote repository
- You'll see all the changes you've made on GitHub
- The very first time you push to a branch, the command usually looks like this:
	- `git push -u origin main`
		- This links your local branch to the remote branch so that the future push commands will automatically apply to this branch without needing to specify it each time
- Once that's set, any commits you push to this branch will just require `git push`
- When that's done, you'll be able to refresh your GitHub repository URl, and see your changes online
## Instructions
- Using the command from this lesson, push your code to GitHub
- Check to make sure this was successful by refreshing the page
# README
## Review
- Create a new repository on local machine
	- `git init`
- Connecting our local repository to GitHub
	- `git remote add origin https://github.com/corinnekost/goan.git`
- Rename a branch to main
	- `git branch -M main`
- Stage and commit changes
	- `git add .`
	- `git commit -m "initial commit"`
- Check the status of our files
	- `git status`
- Push code to GitHub
	- `git push -u origin main`
## Instructions
- Create a new file in your project folder called README.md
- Open the file in your code editor and add some text to describe your repository
- Save the file and commit it to your local repository
- Push the changes to GitHub
