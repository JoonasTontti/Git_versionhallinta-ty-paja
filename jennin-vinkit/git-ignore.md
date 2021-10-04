A gitignore file specifies intentionally untracked files that Git should ignore. Files already tracked by Git are not affected; see the NOTES below for details.

Each line in a gitignore file specifies a pattern. When deciding whether to ignore a path, Git normally checks gitignore patterns from multiple sources, with the following order of precedence, from highest to lowest (within one level of precedence, the last matching pattern decides the outcome):

Patterns read from the command line for those commands that support them.

Patterns read from a .gitignore file in the same directory as the path, or in any parent directory (up to the top-level of the working tree), with patterns in the higher level files being overridden by those in lower level files down to the directory containing the file. These patterns match relative to the location of the .gitignore file. A project normally includes such .gitignore files in its repository, containing patterns for files generated as part of the project build.

Patterns read from $GIT_DIR/info/exclude.

Patterns read from the file specified by the configuration variable core.excludesFile.

