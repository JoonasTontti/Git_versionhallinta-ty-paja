# Resetting files

You’re modifying your code when you suddenly realize that the changes you made are not great, and you’d like to reset them. Rather than clicking undo on everything you edited, you can reset your files to the HEAD of the branch:  

> git reset --hard HEAD  

Or if you want to reset a single file:  

> git checkout HEAD -- path/to/file  

Now, if you already committed your changes, but still want to revert back, you can use:  

> git reset --soft HEAD~1  
