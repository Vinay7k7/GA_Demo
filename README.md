## This is a sample repo that i am trying to import to the github from local 

If you are trying to import the local files to teh github then first you have to do the `git init` command 
and then you will have to run this `git branch -m main` if not the branch will be named as master and it might cause conflict while we are pushing the changes into the main branch in the github.

After that you will add the changed files from you folder into the stage using `git add .` and then you do the commit the changes 
`git commit -m "this is a commint"`.

If you wanna change the account to which you wanna connect to then you have to edit that config file 
`git config --global --edit` and the edited will open in terminal then you press the `i` ti get into insert mode and add the details and to exit then press `esc` button and type `:wq` ti save the changes in the config and and safely exiting the file edited.
and after you add the new account details then you have to run this command `git commit -amend --reset-author`.


Then you push the changes to the main using `push -u origin main`

If there are already changes in the github repo then you have to import those changes into your local for you can run this command 
`git pull origin main --rebase`

And you want to push the changes that you have got in your local repo irrespective of what changes you have got in the github then 
`git push -u origin main --force` this will forcefully pushes the changes in the remote github .



✅ So, the flow is:

git fetch origin

Decide:

git merge origin/main → take everything

git cherry-pick <hash> → take specific commits

git checkout origin/main -- fileX → take specific files[Local Branch]        main
        │
        ├── your commits you’re working on
        │
        ▼
[Remote-tracking]     origin/main
        │   (a bookmark in your local repo)
        ▼
[Remote on GitHub]    main (on GitHub’s server)


Working Directory
      │
      └─(git add .)→ Staging Area
                       │
      └─(git commit)→ Local branch main
                           │
      └─(git push) → GitHub main (remote)
                           │
      └─origin/main (local remote-tracking) ← updated automatically after push/fetch.


vinay 
