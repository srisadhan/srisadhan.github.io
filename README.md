# Steps to build website on local server

## Using Rstudio
install the blogdown package.
- build website : blogdown::build_site() : This will create a folder named public in the repository 
- start server : blogdown::serve_site()
- stop server : blogdown::stop_server()

## Using Hugo in terminal
hugo server -D


# Steps to update the github.io
**The location of the personal website in my drive is C:/Hugo/Sites/personal-website**

## There are two major steps:
### Step 1: Update the personal-website repository
- Check the repository origin : "git remote -v" (if the head directs to some other repo other than "personal-website", git remote add origin <repository path on github>)
- initialize the repository   : "git init"
- update the local repository : "git pull" 
- add the local files         : "git add ." (public folder will not be added as it is ignored in gitignore)
- commit the local files      : "git commit -m "Commit message""
- push the files to the repo  : "git push origin master"


### Step 2: Update the srisadha.github.io repository
cd public
- Check the repository origin : "git remote -v" (if the head directs to some other repo other than "srisadhan.github.io", "git remote add origin <repository path on github>" and then "git remote set-url origin <repository path on github>")
- initialize the repository   : "git init"
- update the local repository : "git pull" (if this does not work, do "git pull origin master --allow-unrelated-histories")
- add the local files         : "git add ." (public folder will not be added as it is ignored in gitignore)
- commit the local files      : "git commit -m "Commit message""
- push the files to the repo  : "git push origin master "

### Common issues:
Sometimes the "git pull" or "git pull origin master --allow-unrelated-histories" might not work. In such situations, it is okay to force the local repository to the github repository.

- Check the repository origin : "git remote -v"
- initialize the repository   : "git init"
- add the local files         : "git add ." (public folder will not be added as it is ignored in gitignore)
- commit the local files      : "git commit -m "Commit message""
- push the files to the repo  : "git push --force origin master "
