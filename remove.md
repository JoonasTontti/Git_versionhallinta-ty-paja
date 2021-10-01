# git rm

The "rm" command helps you to remove files from a Git repository. It allows you to not only delete a file from the repository, but also - if you wish - from the filesystem.

Deleting a file from the filesystem can of course easily be done in many other applications, e.g. a text editor, IDE or file browser. But deleting the file from the actual Git repository is a separate task, for which __git rm__ was made.
# Important Options
### <filename>

The name of a file (or multiple files) you want to remove. Naming the file you want to remove can be as simple as providing the filename / path to a single file. But you can also provide multiple filenames (delimited by spaces) or even a wildcard pattern (e.g. __test__.*).
### --cached    

Removes the file only from the Git repository, but not from the filesystem. By default, the __git rm__ command deletes files both from the Git repository as well as the filesystem. Using the __--cached__ flag, the actual file on disk will not be deleted.
### -r  

Recursively removes folders. When a path to a directory is specified, the __-r__ flag allows Git to remove that folder including all its contents.
### --dry-run  

No files are actually removed. With this option (or its shorthand __-n__ notation), you will only see an output of the files that Git would remove - but no files are actually deleted.  
  
# Usage Examples  

To remove a file both from the Git repository and the filesystem, you can use git rm without any parameters (except for the file's name, of course):

> git rm file1.txt  

If you only want to remove the file from the repository, but keep it on the filesystem, you can add the --cached flag:

> git rm file2.txt --cached  

When trying to delete multiple files in a directory or via a glob pattern, you might want to perform a "dry-run" first and see which files would be removed:

> git rm css/* --dry-run  
>rm 'css/about.css'  
>rm 'css/general.css'  