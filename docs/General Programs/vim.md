# Vim Commands

Below are the most useful Vim Commands I've found. Enjoy!

---

# At The Terminal
| Flag              | Description                                                           |
| ----------------- | --------------------------------------------------------------------- |
| `sudo vim [file]` | To write on a read-only file (usually has to be done on system files) |
| `-M` or `-R`      | Open file such that modifications are not allowed                     |
| `-x`              | Activate encryption on file                                           |
| `--version`       | Print your Vim version                                                |

---

# In The File
**Note:**
* A "word" starts/ends at a non-word character, such as a ".", "-", or ")".
* A "WORD" starts/ends strictly with a white-space.
* For most commands below, a number (#) can precede it to repeat that command that # of times.
* There is a difference between typing the capitalized v.s. the non-capitalized version of letter(s)

## Cursor Movement
| Keystrokes | Action                                                 |
| ---------- | ------------------------------------------------------ |
| `h/j/k/l`  | Move cursor left/down/up/right, respectively           |
| `CTRL + d` | Scroll down one half of a screen                       |
| `CTRL + u` | Scroll up one half of a screen                         |
| `CTRL + f` | Scroll **f**orward one screen                          |
| `CTRL + b` | Scroll **b**ack one screen                             |
| `W`        | Move cursor to the (Mctt) beginning of the next WORD   |
| `w`        | Mctt beginning of the next word                        |
| `E`        | Mctt end of the next WORD                              |
| `e`        | Mctt end of the next word                              |
| `B`        | Mctt beginning of the preceding WORD                   |
| `b`        | Mctt beginning of the preceding word                   |
| `0`        | Mctt beginning of the line                             |
| `^`        | Mctt first non-blank character of the line             |
| `$`        | Mctt end of the line                                   |
| `:#`       | Mctt line number `#`                                   |
| `G`        | Mctt beginning of the last line of the file            |
| `gg`       | Mctt beginning of the file                             |
| `%`        | Mctt matching bracket; (){}[]                          |
| `m?`       | Mark the line on where the cursor is with the letter ? |
| `'?`       | Mctt line marked m?                                    |

## Inserting
| Keystrokes | Action                                              |
| ---------- | --------------------------------------------------- |
| `i`        | Insert before cursor                                |
| `I`        | Insert at the first non-blank character of the line |
| `a`        | Append after cursor                                 |
| `A`        | Append at the end of the line                       |
| `o`        | Create a line below, and enter insert mode          |
| `O`        | Create a line above, and enter insert mode          |

## Deleting

**Note:**
* Any command with `d`/`D` can be replaced with `c`/`C`. If you use `c` instead of `d`, you will immediately enter _insert mode_ after deletion.

| Keystrokes | Action                                                              |
| ---------- | ------------------------------------------------------------------- |
| `D`        | Delete all line content after cursor                                |
| `dd`       | Delete your current line                                            |
| `C`        | Delete the contents of line after the cursor, and enter insert mode |
| `cc`       | Delete your current line and enter insert mode                      |
| `x`        | Delete character at cursor                                          |
| `X`        | Delete character before cursor                                      |


## Yanking and Putting
**Note:**
* To yank means to copy, and to put means to paste.
* Deleting acts as _yanking_ too

| Keystrokes | Action                                           |
| ---------- | ------------------------------------------------ |
| `y`        | Yank                                             |
| `yy`       | Yank your current line                           |
| `p`        | Put what was last yanked, after cursor position  |
| `P`        | Put what was last yanked, before cursor position |


## Visual Mode
| Keystrokes | Action                                                                                                       |
| ---------- | ------------------------------------------------------------------------------------------------------------ |
| `v`        | Enter visual mode, where you can select text by moving around with h/j/k/l or other cursor movement commands |
| `V`        | Visually select your line                                                                                    |
| `CTRL + v` | Enter visual block mode (like visual mode, but you highlight text via one block)                             |

## Replacing Text
| Keystrokes | Action                                                          |
| ---------- | --------------------------------------------------------------- |
| `r`        | Replace 1 character                                             |
| `R`        | Replace characters from cursor and onward                       |
| `s`        | Substitute 1 character and continue in insert mode              |
| `S`        | Substitute entire line, beginning at the beginning of line      |
| `J`        | Join current and bottom line into one line                      |
| `~`        | Invert the case (lowercase/uppercase) of your current character |

## Searching
| Keystrokes    | Action                                                                                                                                    |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `/string`     | Search forwards for _string_                                                                                                              |
| `?string`     | Search backwards for _string_                                                                                                             |
| `/\<string/>` | Strictly searching for _string_. This means ignoring words that contain "string" as part of a bigger word (ie. the mother in motherboard) |
| `n`           | Repeat search in the same direction that you initialized                                                                                  |
| `N`           | Repeat search in the opposite direction that you initialized                                                                              |

## Misc. Edits
| Keystrokes   | Action                                        |
| ------------ | --------------------------------------------- |
| `u`          | Undo your last change                         |
| `U`          | Undo all changes done to your current line    |
| `CTRL + r`   | Redo the last undo you did                    |
| `CTRL + a`   | Increment the number under your cursor        |
| `CTRL + x`   | Decrement the number under your cursor        |
| `>>` or `<<` | Shift text to the right or left, respectively |

---

# In Vim's Command Mode

## Files
| Keystrokes    | Action                        |
| ------------- | ----------------------------- |
| `:w`          | Save changes to file          |
| `:wq`         | Save changes to file and quit |
| `ZZ`          | Save changes to file and quit |
| `:w filename` | Save changes to a new file    |
| `:f`          | List file information         |
| `:q!`         | Ignore file changes and quit  |
| `:x`          | Activate encryption           |

## Set
| Keystrokes                          | Action                                                                                |
| ----------------------------------- | ------------------------------------------------------------------------------------- |
| `:set ic` and `:set noic`           | Case sensitive searches                                                               |
| `:set nu` and `:set nonu`           | Display line numbers                                                                  |
| `:set key=`                         | Set the password for your encrypted file. An empty key option will disable encryption |
| `:set list`                         | Show whitespace (kinda)                                                               |
| `:set syntax=[programmingLanguage]` | Set the syntax of your script to that another programming language                    |

## Find and Replace
| Keystrokes       | Action                                                                                                                     |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `%s/aaa/bbb/`    | For all lines in a file, find string 'aaa' an replace with string 'bbb', for the first instance on a line                  |
| `:%s/aaa/bbb/g`  | For all lines in a file, find string 'aaa' an replace with string 'bbb', for all instances on a line                       |
| `:%s/aaa/bbb/gc` | For all lines in a file, find string 'aaa' an replace with string 'bbb', for all instances on a line. Ask for confirmation |
| `:%s/aaa/bbb/gi` | For all lines in a file, find string 'aaa' an replace with string 'bbb', for all instances on a line. Case insensitive     |
| `:#,##stuff`     | Between line # and line ##, do _stuff_, which are the commands listed above (exluding the `%`)                             |

## Misc. Commands
| Keystrokes                    | Action                                                                                                     |
| ----------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `:! command`                  | Run any _command_ inside Vim (Recall, your current directory is with respect to that of your current file) |
| `:synax off` and `:syntax on` | Turn syntax highlighting off and on                                                                        |

---

# Extras

## Settings
* To show line numbers:
	1) Go to `vim ~/.vimrc`
	2) Append `set number`

## Information

* In insert mode, Vim uses some emacs shortcuts. Visit [this page](https://www.gnu.org/software/emacs/manual/html_node/vip/Commands-in-Insert-Mode.html) for more information.
* If you have multiple windows open, `CTRL+w` (when in editing mode) to toggle "Window switch mode" and then use hjkl to move to a specific window.


## External Learning Resources

To learn more advanced VIM commands and get more practice with it, feel free to visit the following resources I found helpful:

* Typing `vimtutor` on the terminal will bring up Vim's mini-tutorial. Note, most commands covered there have been covered here.
* [yolinux](http://www.yolinux.com/TUTORIALS/LinuxTutorialAdvanced_vi.html)
* [vimgenius](http://www.vimgenius.com/)

## Plugins

Explore [vimawesome](https://vimawesome.com/)

