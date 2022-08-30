# Syntax

## General

* To copy text from the terminal, use `CTRL + SHIFT + C`. Likewise, to paste into the terminal, use `CTRL + SHIFT + V`.
* Anatomy of a command: `command -flags --flags args`
    * Single-character flags can be combined (e.g. `-a -b` into `-ab`)
    * Double-character flags indicate a whole word option (e.g. `--clean`)
* For programs that don't have a `man` page, you can try the following: `program -h` or `program --help`
* A single hyphen (`-`) can be followed by multiple **single-character** flags, while a double hyphen (`--`) prefixes a single **multicharacter** option.
* Piping (`|`) connects the input and output of two commands. When piping, the output of the 1st program is sent to the input of the 2nd program.
* To start a program/command in a subshell, end it with an ampersand `&`. This essentially runs it in the _background_.
* If you ever see a `>` in the terminal it's because the shell is now waiting on input.
* **Wildcards**
	* A wildcard is a symbol that takes the place of an unknown character or set of characters. The two most common wildcards are the asterisk (`*`) and question mark (`?`).
	* An `*` represents any number of unknown characters. Use it at the end of an incomplete filename if you're only interested in filenames that begin with what came before the `*`. The ordering works vice versa too.
	* An `?` represents _one_ unknown character. Use it when you're unsure of a few characters. You can have multiple `?` adjacent to eachother.https://ss64.com/bash/
* `my\ new\ file.txt` or `"my new file.txt"` is an example of how to use literal spaces.
* Operators used to combine commands:
	* `A ; B ` -- Run A and then B, regardless if A succeeds or fails
	* `A && B`  -- Run B only if A succeeds (acts like an AND)
	* `A || B`  -- Run B only if A fails (acts like an OR)

* `sh` vs `./`:
	* Running `sh script` makes dash interpret that script
	* `./ script` tries to find out which interpreter to use by looking at the first line (the bang line, e.g. `#!/bin/bash`), as opposed to running that script.

* Difference between **sourcing** and **executing** a script:
	* Sourcing a script will run the commands in the _current_ shell process, and changes to the environment take effect only in the current shell.
	* Executing a script will run the commands in a _new_ shell, and when the script is done the new shell is terminated
	* **Rule of thumb**: Use source if you want the script to change the environment in your currently running shell, use execute otherwise.
* To have a command span multiple lines, use a backslash (`\`) at the end of each line you're using _or_ a single quote (`'`) at the start and end lines. (With this, your're basically escaping the ENTER key)
* **Command substitution** allows the output of a command to replace the command itself. This can be done as follows: `$(command)` or `` `command` ``
* **Process substitution** allows the input or output of a command to appear as a file. If `>(list)` is used, writing to the file will provide input for a list. If `<(list)` is used, the file passed as an argument will be read to obtain the output of list. [This one needs a bit more explaining]


## Directory Shortcuts

| Directory | Where it leads to |
| --- | --- |
| `~` | Home directory |
| `/` | Root directory |
| `.` | Working (or current) directory |
| `..` | Parent directory |
| `-` | Previous directory (only for cd) |


## Brace Expansion

* Below brace exanpsion will be described via the following set of examples
* Take careful notice on the spacing, it's important

| Example | Result and/or Comments |
| --- | --- |
| `echo "I love "{Bach,Beethoven,Brahms}` | "I love Bach I love Beethoven I love Brahms" |
| `echo {a..z}` | "a b c d e f g h i j k l m n o p q r s t u v w x y z" |
| `echo {1..9}` | "1 2 3 4 5 6 7 8 9" |
| `mkdir {2008..2017}-{01-12}` |  Makes directories for all 12 months in all those years |