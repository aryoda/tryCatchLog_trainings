Collection of Git submodule commands for this repository
========================================================



```{bash}
# Add tryCatchLog as submodule
# (required only once)
git submodule add https://github.com/aryoda/tryCatchLog.git tryCatchLog
```



```{bash}
# Install the submodules after cloning the repository
git submodule update --init
```



```{bash}
# Show the status of the submodules (mainly the referenced commit number)
git submodule summary
```



```{bash}
# Get or reset the submodule files to the referenced commit version.
# Even if you commit changes to the submodule, those changes will quite possibly be lost
# the next time you run git submodule update!
git submodule update
```



```{bash}
# Commit and push changes within a submodule
cd tryCatchLog
git add .
git status
git commit -m "commit message"
git push
```



```{bash}
# Publishing Submodule Changes before pushing the master project
# => otherwise other users who check out your changes don't see the submodule changes
#    (since they exist only in your local repo)
# Ask Git to check that all your submodules have been pushed properly before pushing the main project
git push --recurse-submodules=check
# "check" means to fail if committed submodule changes exist that are not yet pushed
git push --recurse-submodules=on-demand
# "on-demand" does push submodules automatically
```


```{bash}
# Aliases to make your live easier...
git config alias.supdate 'submodule update --remote --merge'



```{bash}
# Getting updates from the upstream of the submodule:
# Go into the directory and run git fetch and git merge the upstream branch to update the local code.
# Eeasier way to do this as well, if you prefer to not manually fetch and merge in the subdirectory:
cd <workspace root>
# the following command does only work if you are in the parent project!
# It updates ALL submodules!
# Local changes in the submodules are merged with the upstream changes.
git submodule update --remote --merge
```



# Links

https://git-scm.com/book/en/v2/Git-Tools-Submodules

