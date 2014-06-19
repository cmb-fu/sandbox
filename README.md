let this be the master repo. It contains two git submodules, which have are
themselves git repos, existing at an independant location and may have therefor
their own issue tracker/wiki etc. on github.

After cloning this, you have to initialize and update the submodule once:
    
    git submodule init
    git submodule update

This will init all submodules in the the current repo and update them to their
current HEAD.
