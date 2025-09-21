## This is a sample repo that i am trying to import to the github from local 

If you are trying to import the local files to teh github then first you have to do the `git init` command 
and then you will have to run this `git branch -m main` if not the branch will be named as master and it might cause conflict while we are pushing the changes into the main branch in the github.

After that you will add the changed files from you folder into the stage using `git add .` and then you do the commit the changes 
`git commit -m "this is a commint"`.

If you wanna change the account to which you wanna connect to then you have to edit that config file 
`git config --global --edit` and the edited will open in terminal then you press the `i` ti get into insert mode and add the details and to exit then press `esc` button and type `:wq` ti save the changes in the config and and safely exiting the file edited.
and after you add the new account details then you have to run this command `git commit -amend --reset-author`.


Then you push the changes to the main using `push -u origin main`

