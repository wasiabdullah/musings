## Git learning 

`git init`
to initilize

`git log`  

`git log --all --graph`  to view logs


`git push origin master`  

`git push origin master --set --upstream`
to set remote repo to be pushed to 
after this can simply use 
git push


### git only pushes commits . It will only push to remote repo when changes are added and committed.

to force push comited use
`git push origin master -f`

### Remote tracking branches do not update automatically  
`git fetch` to update local branch to get up to remote 

`git pull origin master` to pull cahnges from remote to local repo  

 `git pull origin master --set --upstream` to make shortcut  


