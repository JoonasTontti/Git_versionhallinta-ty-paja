You can query/set/replace/unset options with this command. The name is actually the section and the key separated by a dot, and the value will be escaped.

Multiple lines can be added to an option by using the --add option. If you want to update or unset an option which can occur on multiple lines, a value-pattern (which is an extended regular expression, unless the --fixed-value option is given) needs to be given. Only the existing values that match the pattern are updated or unset. If you want to handle the lines that do not match the pattern, just prepend a single exclamation mark in front (see also EXAMPLES), but note that this only works when the --fixed-value option is not in use.

The --type="type" option instructs git config to ensure that incoming and outgoing values are canonicalize-able under the given "type". If no --type="type" is given, no canonicalization will be performed. Callers may unset an existing --type specifier with --no-type.

When reading, the values are read from the system, global and repository local configuration files by default, and options --system, --global, --local, --worktree and --file "filename" can be used to tell the command to read from only that location (see FILES).

When writing, the new value is written to the repository local configuration file by default, and options --system, --global, --worktree, --file "filename" can be used to tell the command to write to that location (you can say --local but that is the default).