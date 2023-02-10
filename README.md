
# How to use SSH for git/github without Error
## steps: 
## 1: look for .ssh folder inside c:/users/current_user/.ssh if not found, create it
## 2: git bash there
## 3: type > ssh-keygen -t rsa -b 4096 -C "your_email@example.com"  then press enter
## 4: press enter at each prompt until it shows an image in box
## 5: type > cat id_rsa.pub , this will bring out your public key, copy it by 
##      right  clickig and selecting copy
## 6: go to your gitub setting, select ssh and gpg key, then on the first input,    type a name for this ssh key, on the second input, paste the ssh key you copied from git bash, make sure you remove the extral horizontal space before use create the key, verify and your ssh key is linked

## 7: back to git bash type > eval "$(ssh-agent -s)" then hit enter
## 8: on git bash type > ssh-add ~/.ssh/id_rsa then hit enter
## 9: on git bash type > ssh -T git@github.com then hit enter, it will bring out a  prumpt, type yes and hit enter, the it will bring out a message like: Hi  your_git_username, you have successfully authenticated, ...
## 10: create a git repo, then copy the ssh link and then:
 ##  a: open a folder in vscode
  ## b: on vscode terminal or git bash for this folder, type
  ## c: git init then enter
 ##  d: create and index.html file, create a simple html content and save
  ## e: git add . then enter
  ## f: git commit -m "version 1" then enter
  ## g: git remote add origin ssh_link_you_copied the enter
  ## h: git branch theb enter , note your current branch in green after an *
  ## i: git push -u origin your_branch_name_without_*
  ## j: next time you want to push changes, repeat steps: e,f, and i. but in step i you can simply use > git push then enter

# Note if your internet connection is via proxy or no or poor internect connection: you'll get an error like
# fatal: Could not read from remote repository.

# Please make sure you have the correct access rights
# and the repository exists.

## This problem stressed me for 7 days. Now i have told you, enyoy!
## spacial thanks to github docs on ssh and some youtube videos

