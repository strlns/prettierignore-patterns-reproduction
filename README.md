Was meant to reproduce a problem / difference between `.prettierignore` and `.gitignore`.

There is no such difference, the problem was me.

Git-SCM documentation on `.gitignore`:

 > It is not possible to re-include a file if a parent directory of that file is excluded. Git doesn’t list excluded directories for performance reasons, so any patterns on contained files have no effect, no matter where they are defined. 
 
This doesn't affect parent directories which have been included through the `/*` wildcard rule, but all explicitly ignored directories.

My two files had different directory hierarchies.
