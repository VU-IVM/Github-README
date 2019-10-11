# VU-IVM-README

Here we explain how you can 'connect' your repository to the VU-IVM page.

## Option 1: Connect an existing local repository

git init
git add .
git commit -m "First commit”
git branch -v # verifies the new local branch
*Now you have a local branch called master, now we also need to connect the local version control to a remote URL.
Go to https://github.com/VU-IVM
Click New (green icon, on the right of VU-IVM Github page)
Fill in Repository name
Add description (optional)
Optional to Initialize this repository with a README.
If you initialized a repo, click on the green Clone or Download button and copy the Github-link, if not, you enter a webpage with more detailed instruction how to set up you repo. 
You only have to copy the Github-link, .e.g. https://github.com/VU-IVM/CIP_drought_impact.git
Now you can connect you local folder to the remote repository.
git remote add origin https://github.com/VU-IVM/CIP_drought_impact.git
git remote -v # verifies the new remote URL
git push -u origin master
Pushes the changes in your local repository up to the remote repository you specified as origin
You can also fix to what branch you are pushing by:
