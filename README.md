let this be the master repo. It contains two git submodules, which have are
themselves git repos, existing at an independant location and may have therefor
their own issue tracker/wiki etc. on github.

After cloning this, you have to initialize and update the submodule once:
    
    git submodule init
    git submodule update

This will init all submodules in the the current repo and update them to their
current HEAD.

Note, that the state of initialization of the submodules is preserved in the master
repo. So if new code is pushed to the submodule repositories, one needs to 
manually update (or e.g. via an post-commit hook script) those:

   git submodule foreach git pull origin master

After this command you have to commit the new pulled in changes to make them 
permanent.
