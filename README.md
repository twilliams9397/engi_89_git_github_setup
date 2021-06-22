# This is our Git and Github set up documentation

- to download Git, click the following link and follow the necessary steps [gitdownload](https://git-scm.com/downloads)
- make sure you have an account on [Github](https://github.com)
- before starting any work/documentation SSH key pairs must be created in order for you local host (laptop/pc) to communicate with Github
- the image below shows how a local host communicates with Github:

![img_1.png](img_1.png)

### SSH keys

- open terminal (Mac) or Gitbash (windows) and create a new directory `mkdir .ssh`
- paste the below line of code when in this directory, using the email address associated with you Github account:

`ssh-keygen -t ed25519 -C "your_email@example.com"`

- when prompted to `Enter a file in which to save the key (/Users/you/.ssh/id_ed25519):` press `enter`
- when prompted to `Enter passphrase (empty for no passphrase):` either enter a secure passphrase or press `enter` to leave it blank
- repeat the above step when prompted `Enter same passphrase again: `
- using terminal/Gitbash `cd` command, access the `.ssh` folder which is where the keys are stored
- in your Github account, in the `settings` tab navigate to the `SSH and GPG keys`
- when in the `ssh` folder use the `ls` command to return both parts of the key
- copy and paste the `.pub` key into the `Github add SSH key` section with an identifiable name and click `add`
- once this key has been added, the Git commands can be used to push data into Github repositories
 
**for more terminal commands try [this](https://github.com/twilliams9397/eng89_markdown_documentation/blob/main/Linux_basics.md)**
### Repositories

- Repositories are created within your Github account
- on creating a new repository, make a note of the git remote command, ensuring SSH is selected:

`git remote add origin git@github.com:your_username/repository_name.git`

### Pushing Data in a New Repository
these commands will work either in the console or in Pycharm
- `git init` initialises the repository in the command line
- `git add` adds files to list to be uploaded - either all files `git add .` or specifics `git add file_name` 
- `git commit -m "descriptive message` commits all files in the directory
- `git branch -M main` ensures you are working on the main branch 
- this is when you run the above `git remote` command
- `git push -u origin main` pushes all selected files into the Github repository
- to check which files are yet to be pushed or slected use `git status`

when adding files to a repostiory that has been previosuly used, only the `git add`, `git commit` and `git push` commands are necessary
