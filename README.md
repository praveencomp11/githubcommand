# githubcommand


# To clean untracked files
    git reset –hard
    git clean -fxd



# Save Stashed Changes and Pop Them Into a Different Branch
# You can quite simply do git stash save on the branch where you have the changes, and then do git stash pop on the branch you want the changes to be in. For example:

    git stash save
    git checkout destination-branch
    git stash pop


# Apply Stashed Changes to a New Branch
# If you wish to apply stashed changes to a new branch, you can simply create a branch from a stash like so:

    git stash
    git stash branch new-branch
    
    
    # As you can see, you first need to stash changes before you can apply them to a new branch when using git stash branch.
    
    # Apply Stashed Changes to an Existing Branch
    # If the branch you wish to apply stashed changes to already exists, you could use a temporary branch to help add the stashed changes to it like so:
    
    git stash
    git stash branch temp-branch
    
    git add .
    git commit
    
    git checkout destination-branch
    git merge temp-branch
    
    git branch -D temp-branch
