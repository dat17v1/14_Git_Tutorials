# Rename a remote repositorys URL

1. Open Terminal.
1. Change the current working directory to your local project.
1. List your existing remotes in order to get the name of the remote you want to change.    
````
$ git remote -v
origin	https://github.com/dat17v1/01_introduction.git (fetch)
origin	https://github.com/dat17v1/01_introduction.git (push)    
````   
in this case the name is 'origin'    

3. Change your remote's with the git remote set-url command.  
````   
$ git remote set-url origin https://bitbucket.com/dat17v1/01_introduction.git    
````   
4. Verify that the remote URL has changed.    
````   
git remote -v
# Verify new remote URL
origin  https://bitbucket.com/dat17v1/01_introduction.git (fetch)
origin  https://bitbucket.com/dat17v1/01_introduction.git (push)    
````   

_ edited from https://help.github.com/articles/changing-a-remote-s-url/ _
