# VU-IVM Github README 

Here we explain how you can connect your repository to the VU-IVM page. \

## Option 1: Fork your existing Github repository
Become a member, send an email to one of the repo maintainers (e.g. sem.vijverberg@vu.nl). \
Once you are part of the VU-IVM Github institution: \
Go to personal github repo \
Click on Fork (upper right of page), then you should see the organization which you are linked to. \

Generally forked repos are used to collaborate with other people on the same package. There is an original repo, and there are forked repos which can add features and request to merge the new features into the original repo (pull request, original <- forked). Choosing this option 1 means that other collaborators will still need to fork from your original repo and not from the already forked one. I'm honestly not really sure what is the best way to go, input is welcome! \

Anywho, to keep a forked repo up to date with the original, you have to clone the forked repo to your local machine. Then add the remote branch of the original repo: \
git remote add original https://github.com/{user-name}/{repo-name}.git \
Now you have two remote branch: \
git remote -v
To pull the most recent updates from the original repo: \
git pull original master \
To push these updates to the forked repo on the IVM Github: \
git push origin master



## Option 2: Connect an existing local repository 

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
If you initialized a repo, click on the green Clone or Download button and copy the Github-link, if not, you enter a webpage with more detailed instruction how to set up you repo. \
You only have to copy the Github-link, .e.g. https://github.com/VU-IVM/{your_repo_name}.git \
Now you can connect you local folder to the remote repository. \
git remote add origin https://github.com/VU-IVM/{your_repo_name}.git \
git remote -v # verifies the new remote URL \
git push -u origin master \
Pushes the changes in your local repository up to the remote repository you specified as origin \
After you have run git push -u origin master, it will automaticallly push your next updates to the origin if you only write: \
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
