# GIT
| command | explanation |
| ------ | ------ |
|`git config`|this can be used to set config `--global` or to the working directory|
|`git init` | Initialize a git local repo [creating empty repository]|
|`git clone`| download a project from remote|
|`git add`| prepare a file (to Staging)|
|`git commit`| commit a file to the local repo|

## _Setting Global Config_
| command | 
| ------ | 
|`git config --global user.name "veer"`| 
|`git config --global user.email "veeresh.bikkaneti@gmail.com"`|
## Edit Global Config
| command | explanation |
| ------ | ------ |
|`git --edit --global`|will open edit config in default editor|
| ------ | you can choose to open it using VScode by typing `code`|
| ------ | Setting VS code as default editor |
| ------ | Add VScode to env variables |
| ------ | `git config --global core.editor "code --wait --new-window"` |

| command | explanation |
| ------ | ------ |
|`git init`| by default it will create a master branch|
|`git status`|shows untracked files|
| `git add <filename>` |add single file|
|`git add .` |add all files|
|`git commit -m "Nww commit"`| commit new files|
|`git commit -am "all modified Files"`| commit all new and modified files|
|`git log` | check the log of commits|


### SSH Key Vs HTTP
- HTTP required to enter user cred everytime you push some code;
- SSH on contrary will keep the connection alive using ssh key
#### _SSH Key setup_
| command | explanation |
| ------ | ------ |
|` ls -al ~/.ssh`|check if SSH key is already generated. SSH folder to keep Secure Shell connection |
|`ssh-keygen -t rsa -b 4096 -C "veeresh.bikkaneti@gmail.com"`|
| add SSH key to SSH Agent||
| `eval $(ssh-agent -s)` |SSH agent is running|
|`ssh-add ~/.ssh/id_rsa`|Adding SSH key using SSH-Add to the specified directory|
|let the github know SSH key was added|
| usually created in C:\Users\vneti\.ssh|
| copy the file contents of `id_rsa.pub` file and paste it in github->settings->SSH and GPG keys->SSH keys ->New SSH Key|
|`ssh -T git@github.com`| authenticates your machines to github with SSH key we generated.|

> The overriding design goal for Markdown's


## Commands for working with local Branches
| command | explanation |
| ------ | ------ |
|`git branch [branch-name]`| creates branch in your local|
|`git checkout [branch-name]`| switch to the local branch you want to work with, files in the working directory are replaced with the onces in that branch|
|` git checkout -b [branchName]`| will create a new branch, switch and checkout the code to the new branch|
|`git push -U [origin] [branch]`| when we create a new new branch, this is not pushed into the github, only when we use -U, specify orign and branch|



