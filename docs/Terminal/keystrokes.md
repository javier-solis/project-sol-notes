# Keystrokes

* These keystrokes are applicable in Bash's Emacs-mode.
* This list is not complete, these keystrokes represent the ones that I most often use and recommend memorizing.
* I organized them in order of usage
* Formatting:
    * Capitalized words represent special keyboard keys. Some are self explanatory (e.g. `SHIFT` is the shift key) while others may be confusing. Those are described below:
        * `UP` =  up arrow key
        * `DOWN` =  down arrow key
        * `LEFT` =  left arrow key
        * `RIGHT` =  right arrow key
    * Keystrokes that require multiple keys combines those with plus signs (i.e. `+`). Literal plus keys are denoted with `PLUS`.
    * Lowercase letters represent pressing the letter in its lowercase form (i.e. holding `SHIFT` while pressing the letter)
    * Capitalized letters represent pressing the letter in its capitalized form (i.e. holding `SHIFT` while pressing the letter)
    * Bold words/letters in the action description are used to point out the keystroke's main attribute(s)

---

# Frequenly Used

## Cursor Movement

| Keystrokes | Action: "Move cursor..." |
| --- | --- |
| `ALT + f` | one word **f**orward |
| `ALT + b` | one word **b**ackward |
| `CTRL + e` | to the **e**nd of the line |
| `CTRL + a` | to the st**a**rt of the line |
| `CTRL + p` or `UP` | one line u**p** |
| `CTRL + n` or `DOWN` | one line dow**n** |

## Deletion and Buffers

| Keystrokes | Action |
| --- | --- |
| `CTRL + w` |  Delete the **word** portion that's **before** the cursor (If cursor is at a space, deletes all of word) |
| `ALT  + d` |  Delete the **word** portion that's **after** the cursor (If cursor is at a space, deletes all of word) |
| `CTRL + u` | Delete text from the **beginning** of the line up to the **cursor** |
| `CTRL + k` | Delete text from the **cursor** up to the **end** of the line |
| `CTRL + y` | **Y**ank (copy) the content of the buffer, and **push** (paste) it at the cursor |

---

# Moderately Used

## Process Control

| Keystrokes | Action |
| --- | --- |
| `CTRL + c` | Kill whatever process is running in the foreground |
| `CTRL + z` | Pause the current foreground process, and send it to the background |
| `CTRL + d` | Acts as the end-of-input character, performing the equivalent of a typical program's `q`, `quit`, `exit`, etc. With this, you're telling a process that your input is finished. Psrticularly useful for closing the terminal/other processes (Python subshell, etc.) |
| `CTRL + s` | **Stop all output** to the screen. This is useful when running commands that are very verbose |
| `CTRL + q` | **Resume output** to the screen (after having stopped it with `CTRL + s`) |

## Extras

| Keystrokes | Action |
| --- | --- |
| `CTRL + l` | Clear the screen (history isn't erased, it's just pushed up)|
| `!!` | Run the previous command you ran |
| `^abc^xyz` | Run the previous command you ran but replace the first occurrence of `abc` with `xyz` |
| `CTRL + _` | Undo the last letter(s) you typed into the command line |
| `Alt + r` | Cancel all changes you've made to your line, putting it back into its original form |

---

# Rarely Used

## Searching

| Keystrokes | Action |
| --- | --- |
| `CTRL + r` | Search "up" through your terminal history |
| `CTRL + j` | Leave history searching mode, without running a command |
| `CTRL + g` | Cancel the search and return to your original line |
| `CTRL + o` | Run the command that you found |

## Special Keys

| Keystrokes  | Action |
| --- | --- |
| `CTRL + j` or `CTRL + m` | Same as ENTER/RETURN key |
| `CTRL + [` | Same as the `ESC` key |

---

# Further Suggestions

## Emacs-Mode vs Vi-Mode

All the above keystrokes assume that Bash is running in its default Emacs setting. It's possible to switch to Vi shortcuts as so: `set -o vi`. Then, return to Emacs is via: `set -o emacs`.

## More Keystrokes

Below are external resources where you can find a variety of more keystrokes:
* [Github Gift Page](https://gist.github.com/tuxfight3r/60051ac67c5f0445efee)
* [ss64](https://ss64.com/bash/syntax-keyboard.html)
