# Commands

## Core Commands

| Command | Result |
| --- | --- |
| `man` | Open the manual/help page for a given command |
| `whatis` | A TL;DR `man` page for a command |
| `cd` | Change directory |
| `ls` | List directories |
| `pwd` | Print working Directory |
| `rm` | Remove file |
| `rmdir` | Remove directory |
| `mkdir` | Make directory |
| `mv` | Move directory. Can be used to rename files too (set the source as the destination) |


## Good to Know Commands/Subcommands

| Command | Result |
| --- | --- |
| `rm -r` | Remove a directory and all files that are in it. Also recursively deletes nested directories |
| `rm -I` or `rm -i` | To confirm each file removal |
| `rm -v` | State that the file was removed |
| `rm -f ` | To avoid being asked about removing files, add the -f ("force") option. |
| `grep` | Search for text in files |
| `find` | Search for filenames, inside the directory you're currently at |
| `file name` | Tells you the file type of _name_ |
| `which <...>` | Used to find the location of executable functions |
| `echo` | Display text/string that is passed as an argument |
| `echo "Hello!" >> myfile.txt` | Append text to the end of the file. Note that `>>` means adding a new line to the file while `>` simply overwrites everything.|
| `echo $(( stuff ))` | To do math with integers |
| `echo $VAR` | Output the value of the _VAR_ variable. For instance. `echo $HOME` tells you what your home directory is |
| `echo -n [...]` | Do not output to a newline, output to the current one |
| `echo -n [...]` | Enable the interpretation of backslash escapes |
| `history` | Print your command line history |
| `ls -l` | Print a list of directories, but with more of their metadata |
| `ls -lh` | Same as above, but more human-readable | mkdir -p _parent/child_ | Create a “chain” of directories |
| `ls -F` | Tell the difference between files and directories |
| `ls -a`| Show all files, including dot files |
| `ls -t` | New files appear first |
| `ls -R` | Recursively list (see subfolders and their contents, recursively)|
| `ln -s <full file directory> <new directory>shortcut_name` | Create a symbolic (or soft) link. The file directory should be written out in full (ie. including /home/user/…). Note, the directory of a shortcut is often placed in the `/usr/bin` folder, so you can type "shortcut_name" anywhere in the terminal to access it. Note,  A symbolic or soft link is an actual link to the original file, whereas a hard link is a mirror copy of the original file.|
| `readlink -m <shortcut name>` | Prints the directory of where that shortcut name is |
| `cp `<target file/directory>` `<destination directory>` | Copy _target file/directory_ to _destination directory_ |
| `cp -r <...> <...>` | Copy directories along with their contents |
| `diff --report-identical-files <...> <...>` | Compares two files to see if they match in content |
| `head` | Print the first 10 lines of a file. You can also add _-n #_, where # is the amount of lines you'd like to show |
| `tail` | Print the last 10 lines of a file. You can add -n # too
| `touch file.txt` | Creates a file with that name. Also updates the aces data/ modification date. |
| `less` | Eextends the capabilities of more. The latter was created to view the content of a file one screenful at a time. less adds features such as backward movements and better memory management. Usually used for longer files |
| `cat` | _Cat_enates (concatenates) files and prints the result onto the standard output. This is usally used for viewing a short file on the terminal |
| `mkdir -p parent/child` | Create a “chain” of directories |
| `rmdir` | Remove a directory |
| `mount`/`umount` | Mount/ unmount devices |
| `jobs` | Lists all jobs |
| `bg #` | Places the current (if there's one) or specified job in the background, where # is the job ID
| `fg #` | Brings the current (if there's one) or s |ecified job into the foreground, where n is the job ID |
| `kill %#`| Terminate a specific job # |
| `killall` | Kill all jobs |
| `clear` | Clear the screen |


## Rare But Powerful Commands

| Command | Description |
| --- | --- |
| `wget <url>` | Used to download files from the internet |
| `tee file` | Output to terminal and save to file |
| `nmcli` | Network/wifi/ethernet information |
| `HISTTIMEFORMAT="%F %T "`| Set the Bash history to show a timestamp for your command history (for the current terminal session only). Now type history and you should see timestamp for your Bash history. |
| `export` | Export is 11v a built-in command of the Bash shell. It is used to mark variables and functions to be passed to child processes. Examples include $HOME and $PATH. |
| `wc` | Print info about a file |
| `df` | Display disk space usage |
| `chmod +x [file]`| To make _file_ executable |
| `lsusb` | Display which USB ports are being used and by what |
| `passwd` | To change your password |
| `uname` | To see what kernel version you have on your system |
| `top` | Show processes information |
| `env` | Show environment variables |
| `sort` | Sort lines of text files |


# More!

For an overwhelming number of other commands, I recommend this [source](https://ss64.com/bash/).

