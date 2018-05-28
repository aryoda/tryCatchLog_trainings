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
# Get or reset the submodule files to the referenced commit version
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
# Getting updates from the upstream of the submodule
cd <workspace root>  # the following command does only work if you are in the parent project!
git submodule update --remote --merge
```



