# VU-IVM Github README 

Here we explain how you can connect your repository to the VU-IVM page. \

## Option 1: Connect an existing local Github repository 
Preferably, I would like to have one single version online. The only way to do this is perhaps to Transfer ownership (which I find a bit scary). \
What I did now is create a new empty VU-IVM repo, via: \
Go to https://github.com/VU-IVM \
Click New (green icon, on the right of VU-IVM Github page) \
Fill in Repository name \
Add description (optional) \
Do not initialized the repo \
Copy the Github-link, .e.g. https://github.com/VU-IVM/{your_repo_name}.git \
Now you can connect you local folder (that is already connected to a github repository) to the new IVM remote. \
git remote add IVM https://github.com/VU-IVM/{your_repo_name}.git \
git remote -v # verifies the new remote URL \

Add .gitignore (optional) \
touch .gitignore \
vi .gitignore (enters terminal-based text editor, press i to insert text, esc to exit text editing mode, once out of text editing mode :w to write, :q to quit) \
e.g. to avoid pushing a folder called Answers \
press i type Anwsers/ press esc type :wq (to write and quit). \

git push IVM master \


## Option 2: Connect an existing non-Github local repository 

git init \
git add . \
git commit -m "First commit” \
git branch -v # verifies the new local branch \ 
*Now you have a local branch called master, now we also need to connect the local version control to a remote URL. \
Go to https://github.com/VU-IVM \
Click New (green icon, on the right of VU-IVM Github page) \
Fill in Repository name \
Add description (optional) \
Optional to Initialize this repository with a README. \
If you initialized a repo, click on the green Clone or Download button and copy the Github-link. \
if you do not Initialize the repo, just the empty folder is created. \
You enter a webpage with more detailed instruction how to set up you repo. \
Copy the Github-link, .e.g. https://github.com/VU-IVM/{your_repo_name}.git \
Now you can connect you local folder to the remote repository. \
git remote add origin https://github.com/VU-IVM/{your_repo_name}.git \
git remote -v # verifies the new remote URL \
git push -u origin master \
Pushes the changes in your local repository up to the remote repository you specified as origin \
After you have run git push -u origin master, the -u flag ensures that it will automaticallly push your next updates to the origin if you only write: \
git push


# Connect your practicum assignment to Binder:
Binder builds a (python) environment with all its dependencies 'in the cloud'. Although it is not perfectly stable, it avoids set-up time when installing python locally.

https://mybinder.org/ \
Fill in you Git-URL: \
https://github.com/VU-IVM/{your_repo_name}.git \
the branch you want to publish: \
generally the master branch
Copy the Binder badge into your readme: \
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/VU-IVM/{your_repo_name}.git/master)
