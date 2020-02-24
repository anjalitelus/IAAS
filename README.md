<<<<<<< HEAD
# IAAS
IAAS
victor  
angie 
test comments

=======
# ISSA development
the project is aiming to develop an ISSA cloud platform  to manage and monitor Telus SD-WAN services

# Prerequisites
in order to make team memebers work together, all the collaborators will follow the same process about how to use the repo and update docs, below are the steps about how to work togther using the repo

## step1: create a github account on github website
please go to github website [github][github] and create an account.  

## Step2: download and install git client software in your PC
for Windows, please download and install the git client via the link: [git for windows][git-for-windows].
git client  is comprised of three types of client softwares: Git Bash, Git Gui and Git CMD, Git Bash is recommended to use, below is how a Git Bash looks like on windows: ![git-client][git-client]

for Linux, please refer to the related Linux OS installation instruction, below is an example to install git in Linux Centos 7
```centos7
#yum -y install git  
```
## Step3: configure your git client
- setup global parameters 
```git
! setup username and email 
git config --global user.name "<username>"
git config --global user.email "<email>"  
! verify the configuration
git config --list
```  
- generate ssh key
```
cd ~
ssh-keygen -t rsa
cd .ssh
cat id_rsa.pub
```
- associate the ssh key to your github account
copy the key from the output of command 'cat id_rsa.pub'' and paste it to your github account, below is how to do it
- login the github with your account
- on dashboard, navigate to settings
![ssh-key-settings][ssh-key-settings-1]  
and fill the Title and paste the key into the key area
![ssh-key-settings][ssh-key-settings-2]
 

## step4: fork the IAAS repo to your github account
in order to fork the IAAS repo to your github account, you need to login github website [github][github] with your account first.
Then go to the link: [IAAS repository][IAAS-repo] and click the button "fork" 
below is a snapshot:
![fork][fork]

## step5: clone the forked repo from your account to your PC
open your Git Bash and follow the steps below:
```
! create a root folder in your PC for all your repos
mkdir <folder name>
cd <folder>
! clone the repo 
git clone https://github.com/<your github account username>/IAAS
```

## step6: add remote link of the main repo
open your Git Bash and go to the IAAS repo folder and run the command below to add remote link of the main repo
```
git remote add upstream https://github.com/victor-hgq/IAAS
```
## step7: update your docs to your repo in your github account
when a collaborator create new docs or update existing docs, please push it to your IAAS repo sitting in your account, below is the steps:
```
! please pull the latest repo from the main repo first for the consistence
git pull upsream master
git add .
git commit -m "<commit message>"
git push origin master
```

## step8: send PUll request to merge the updated doc to main repo
- login github with your account
- navigate to your forked IAAS repo
- send pull request as shown as below
![send pull request][new_pull_request.PNG]  


## step9: all collaborator may go through the udpate and add comments

## step10: merge the updated docs into the main repo
the owner of repo will merge the updated docs into the main repo if all collaborators have no objection 







<!--- below is the link for pictures -->
[git-client]: images/git_client.PNG
[github]: https://github.com/
[git-for-windows]: https://git-scm.com/
[IAAS-repo]: https://github.com/victor-hgq/IAAS
[fork]: images/fork.PNG
[ssh-key-settings-1]: images/ssh_settings_1.PNG
[ssh-key-settings-2]: images/ssh_settings_2.PNG
[new_pull_request.PNG]: images/new_pull_request.PNG
>>>>>>> 58bafb696eab4552ce2e968615c1dafc81efe355
