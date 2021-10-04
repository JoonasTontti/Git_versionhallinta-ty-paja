One of the coolest features of the git log command is the graphing feature. The git log graph command creates a graphic overview of how a developer’s various development pipelines have branched and merged over time.


I find it especially impressive how this visual display is done through a decidedly non-visual BASH shell or terminal window. Let’s examine some more features of the git log graph command and how to use it in your code.

n its simplest form, the git log graph command looks like this:

graph@log:~$ git log –graph

git log graph pretty
The git log graph command is too verbose without a pretty switch.
The problem with the basic –graph usage is that the log’s wordiness gets in the way. Instead, match the git log graph command with a pretty one line option to make the output look much nicer:


graph@log:~$ git log –graph pretty=online