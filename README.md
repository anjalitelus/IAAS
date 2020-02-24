# ISSA development
the project is aiming to develop an ISSA cloud platform  to manage and monitor Telus SD-WAN services


# Prerequisites
below is required for all team members
- create a github account on github website (please skip this if you already have an account)  
 please go to github website [github][github] and create an account.
- download and install git client software in PC  
for Windows, please download and install the git client via the link: [git for windows][git-for-windows].
git client  is comprised of three types of client softwares: Git Bash, Git Gui and Git CMD, Git Bash is recommended to use, below is how a Git Bash looks like on windows: ![git-client][git-client]

for Linux, please refer to the related Linux OS installation instruction, below is an example to install git in Linux Centos 7
```centos7
#yum -y install git  
```

- git client initial configuration   
  1. setup global parameters 
```git
! setup username and email 
git config --global user.name "<username>"
git config --global user.email "<email>"  
! verify the configuration
git config --list
```  
  2. generate ssh key
 
```
cd ~
ssh-keygen -t rsa
cd .ssh
cat id_rsa.pub
```
  3. associate the ssh key to your github account
copy the key from the output of command 'cat id_rsa.pub'' and paste it to your github account, below is how to do it
    - login the github with your account
	- on dashboard, navigate to settings
![ssh-key-settings][ssh-key-settings-1]  
and fill the Title and paste the key into the key area
![ssh-key-settings][ssh-key-settings-2]
 


# Workflow 
in order to make all the collabortors co-operate effectively, all the collaborators will follow the same approach about how to use the repo and update docs. forking workflow will be used for this project. below is a diagram about how forkingworkflow works in this project
![workflow][fork_workflow.PNG]

below are the steps about how workflow works
## step1: collaborators fork the IAAS repo to their own github account
in order for a collaborator to fork the IAAS repo from main repo to a collaborator's github account, the collaborator need to login github website [github][github] with their account first.

Then go to the link of main repo: [IAAS repository][IAAS-repo] and click the button "fork" 
below is a snapshot:
![fork][fork]

## step2: clone the forked repo from a collabrator's account to their local PC
open the Git Bash in local PC and follow the steps below:
```
! create a root folder in your PC for all your repos
mkdir <folder name>
cd <folder>
! clone the repo 
git clone https://github.com/<your github account username>/IAAS
```

## step3: add remote link of the main repo
open your Git Bash and go into the IAAS repo folder and run the command below to add remote link of the main repo
```
git remote add upstream https://github.com/victor-hgq/IAAS
```
## step4: a collaborator update docs to their local repo 
when a collaborator create new docs or update existing docs, they will pull the latest repo first then update docs to local repo as shown as below:
```
! please pull the latest repo from the main repo first for the consistence
git pull upsream master
git add .
git commit -m "<commit message>"  
```
## step5: a collaborator push updates to their own forked repo
```
git push origin master
```

## step6: a collabrator create a new pull request 
- a collaborator has to login github with their github account first
- navigate to their forked IAAS repo
- send pull request as shown as below
![send pull request][new_pull_request.PNG]  










<!--- below is the link for pictures -->
[git-client]: images/git_client.PNG
[github]: https://github.com/
[git-for-windows]: https://git-scm.com/
[IAAS-repo]: https://github.com/victor-hgq/IAAS
[fork]: images/fork.PNG
[ssh-key-settings-1]: images/ssh_settings_1.PNG
[ssh-key-settings-2]: images/ssh_settings_2.PNG
[new_pull_request.PNG]: images/new_pull_request.PNG
[fork_workflow.PNG]: images/fork_workflow.PNG