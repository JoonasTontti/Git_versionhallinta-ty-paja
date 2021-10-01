# Set a global .gitignore

If you want to avoid committing files like __.DS_Store__ or Vim __swp__ files, you can set up a global __.gitignore__ file.

Create the file:

>touch ~/.gitignore  

Then run:

>git config --global core.excludesFile ~/.gitignore  

Or manually add the following to your __~/.gitconfig__:

>[core]  
> excludesFile = ~/.gitignore  

You can create a list of the things you want Git to ignore. To learn more, visit https://git-scm.com/docs/gitignore.