## Forking Workflow (Minus the PR)
1. Fork the master branch and clone your forked copy
    ```
    # clone the forked branch
    git clone https://github.com/<YourGitHubUsername>/test.git
    ```  
  * If you anticipate spending considerable amount of time on a change, make sure you keep your local repository up to date  
    ```
    # add upstream repository to remotes
    git remote add upstream https://github.com/FSU-ACM/test.git
    
    # verify that the upstream repository was added
    git remote -v
    ```
  * Whenever you want to update your fork, you will need to fetch from the upstream repository to bring its updated branches and commits
    ```
    # fetch from upstream
    git fetch upstream

    # checkout your master branch and merge upstream's master branch
    git checkout master
    git merge upstream/master
    ```
  * **If there are unique changes to your local master branch, you may have to deal with conflicts. Follow the next section to avoid this.**  
2. Create a branch for the feature you'd like to add/work
    ```
    # make sure you are on master branch
    git checkout master

    # choose a simple name that describes the feature for new branch name
    git branch feature_name

    # checkout your new branch
    # git checkout -b feature_name combines this and the last command
    git checkout feature_name
    ```
3. Once you have completed feature and want to push it to your fork
    ```
    git add <files>
    git commit -m "A useful commit message"
    git push --set-upstream origin feature_name
    ```
