---
Shell Scripting
---
# Bash

## Start up Files
On load as a login shell (e.g. ssh login, tty login or `bash --login`) Bash will source files in the following order:
`/etc/profile` -> `~/.bash_profile` -> `~/.bash_login` -> `~/.profile`
<sub>Note `.profile` is used for all shells while `.bash_profile` is only used for bash</sub>

When invoked as an interactive non-login shell, the `.bashrc` file is sourced.

If changes are made to these files, the file must be either sourced `source <file>` (shorthand `. <file>`) or a new bash session invoked.

Typically a `~/.*profile` file will include a line of:
```sh
if [ -f ~/.bashrc ]; then
	source ~/.bashrc
fi
```
Which ensures that the bashrc is loaded in login shells as well.


