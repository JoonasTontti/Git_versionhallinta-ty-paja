# Stashing uncommitted changes  

If you’re ever working on a feature and need to do an emergency fix on the project, you could run into a problem. You don’t want to commit an unfinished feature, and you also don’t want to lose current changes. The solution is to temporarily remove these changes with the Git stash command:

> git stash  

The git stash command hides changes, giving you a clean working directory and the ability to switch to a new branch to make updates, without having to commit a meaningless snapshot in order to save the current state.

Once you’re done working on a fix and want to revisit your previous changes, you can run:

> git stash pop  

And your changes will be recovered. 

If you no longer need those changes and want to clear the stash stack, you can do so with:

> git stash drop  
