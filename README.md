# :shell: Custom Commands for your Console

### short commands to display cheat-sheets in your CLI (executable from any directory)

What you'll be able to do with it:

- :speech_balloon: **display** cheat sheets by command from anywhere inside your console
- :pencil2: **edit** cheat sheets by command from anywhere inside your console ([show me how](#how-to-edit-contents-of-a-cheat-sheet))
- :new: **create** new commands ([show me how](#how-to-create-a-new-command))

> [!IMPORTANT]
> The main idea of this project is to help beginner developers improving their workflow. The cheat-sheets are a collection of commands/shortcuts that **I** think are useful. If you feel different about it, **you're more than welcome to customize the sheets** ([show me how](#how-to-edit-contents-of-a-cheat-sheet)). You can also rename the commands, therefor change the alias name ([show me how](#how-to-change-a-command-name)).

Available cheat-sheets (customizable):

- CLI-Commands
- GitHub Text Formatting
- JavaScript Conditionals
- JavaScript Loops
- JavaScript Array Methods
- JavaScript Strings
- Special Characters
- Git/GitHub Commands
- VS Code
- _..maybe your own?_

### :arrow_right: [Directly jump to Installation](#installation)

## Quick-Start

To display all available commands:

```
commands
```

**Example1: For useful CLI-Commands**

_type into console:_

```
terminal-tips
```

example Output:

```
                            ╭─────────────────────╮
                               Console Shortcuts
                            ╰─────────────────────╯


+-----------------------------------------------------------------------------------+
|                             FILES / FOLDERS                                       |
+-----------------------------------------------------------------------------------+
| ls                  	     | display files and subdirectories in the directory    |
| ls -a                      | displays hidden files too                            |
| cd                         | Home directory                                       |
| cd [folder]                | Change directory, e.g. cd Documents [TAB to suggest] |
| cd /                       | Root of the drive                                    |
| cd -                       | Previous directory or folder you last browsed        |
| pwd                        | Show your present working directory                  |
| cd ..                      | Move up to the parent directory                      |
| cd ../..                   | Move up two levels                                   |
| mkdir <dir>                | create new folder named <dir>                        |
| mkdir -p <dir>/<dir>       | create nested folders                                |
| mkdir <dir1> <dir2> <dir3> | create several folders at once                       |
| rm <file>                  | remove file                                          |
| rmdir <folder>             | remove folder                                        |
| touch <file>               | create a new file without any extension              |
| cat <file>                 | output the content of <file>                         |
| open [file]                | opens a file                                         |
| open . .                   | opens current directory                              |
| mv <file> <newfilename>    | rename file                                          |
| mv <file> <dir>            | move file to directory (tries overwriting!)          |
| example=„string“;          | stores a string into a variable called example       |
| echo $example;             | prints the string of example to terminal             |
| [cmd] + [Shift] + [.]      | show hidden system files/folders                     |
+-----------------------------------------------------------------------------------+
|                                PATHS                                              |
+-----------------------------------------------------------------------------------+
| echo $PATH                 | show current Paths                                   |
| echo $SHELL                | shows path of/kind of Shell Profile that you use     |
| tr ':' '\n' <<< $PATH      | list Paths in a more structured way                  |
| sudo nano <path>           | add Paths  (<path> eg: Users/user/.bashprofile)      |
+-----------------------------------------------------------------------------------+
|                                SEARCH                                             |
+-----------------------------------------------------------------------------------+
| sudo find / -name [name]   | search your system for a file                        |
+-----------------------------------------------------------------------------------+
|                             CANCEL / EXIT                                         |
+-----------------------------------------------------------------------------------+
| [CTRL] + [C]               | returns                                              |
+-----------------------------------------------------------------------------------+

___________________________________________
commands		show all custom commands

```

**Example 2: JavaScript Loops**

_type into console_

```
js-loops
```

displays to console (extract):

```
╭─────────────────────╮
    JavaScript Loops
╰─────────────────────╯

╭─────────────────────╮
│    Example Array    │
╰─────────────────────╯

let words = ['you', 'can', 'do', 'it'];

╭───────╮
│  for  │
╰───────╯

for (let i=0; i < words.length; i++) {
  console.log(words[i]);
}

// 'you' 'can' 'do' 'it'


╭─────────╮
│ forEach │
╰─────────╯

words.forEach(word => {
  console.log(word);
});

// 'you' 'can' 'do' 'it'


╭───────╮
│ while │
╰───────╯

loops until a condition is true
_________________________________________


let count = 0;

while (count < 4) {
  console.log(words[2]);
  count++;
}

// 'do' 'do' 'do' 'do'


╭───────────╮
│ do...while│
╰───────────╯

same as while loop, but runs at least once
(even if condition is false)
_________________________________________

let x = 1
do {
  console.log(words[2]);
} while (x > 1);

// 'do'


```

**Example 3: GitHub Text-Formatting**

_type into console_

```
gh_format
```

displays to console:

````
******** Text Markup *********

# A first-level heading
## A second-level heading
### A third-level heading

**bold**

_italic_

[```]  (square brackets only here in the Readme file)
codeblock
[```]


********* Ordered List (Numbers) ************

1. element 1
2. element 2
3. element 3

********* Ordered List (Bullet Points) ************

- element 1
- element 2
- element 3

********* Links ********

[Link-Title](URL)

********* Images *******

![description](IMAGE-URL)

******** Emojis ********

:vampire_woman:		shows Vampire Woman
:+1:			shows Thumbs Up Emoji
:heart:			shows Heart Emoji

full list here: https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md
````

## Installation:

> **Note:** So far this is only for MAC/Linux Users (Bash/ZShell)

1. Download all .txt files from ([cheat_sheets](/cheat_sheets/)) and save it to a directory.

2. Figure out if you are using ZShell or Bash:

```
echo $SHELL
```

3. Open your Configuration File:

_For ZShell type:_

```
 nano ~/.zshrc
```

_For Bash type:_

```
 nano ~/.bshrc
```

_Help for GNU:_ [CMD] + [X] to save, press [Y] to save, [ENTER] to confirm

_Alternatively:_ Open configuration with a Code/Text-Editor

or:

```
 open ~/.bshrc
```

4. Add contents of profile.txt ([click here](/console_profile/profile.txt))

   **Important:** Replace the path with the directory where you saved the .txt files / where your shell profile is located!

_example:_

```
# Path Variables

PATH_TO_SHEETS="/Users/mariah/bin/"
PATH_TO_PROFILE="~/.bshrc"
```

You can also cherry-pick depending to your needs :cherries:

For example: If you dont want the react sheet cheat, delete the following lines:

```
# React Cheat-Sheet
alias react-tips='cat '$PATH_TO_SHEETS'react-tips.txt'
```

5. Save configuration file, close and reopen Terminal
6. You can now use these commands in every directory! :space_invader: :space_invader:

## How to change a Command Name?

1. Type in the following command to open your Console profile

```
profile
```

2. Let's say you want to change the command name of 'terminal-tips':

```
# Terminal Cheat-Sheet
alias terminal-tips='cat '$PATH_TO_SHEETS'terminal-tips.txt'
```

Change the Alias name:

```
# Terminal Cheat-Sheet
alias NEWNAME='cat '$PATH_TO_SHEETS'terminal-tips.txt'
```

3. Remember to adjust your list of available commands to not forget the name of your new command

type into console:

```
edit commands
```

## How to edit contents of a cheat sheet?

**By command:**
To edit type following command into console

```
edit <nameofcommand>
```

**Example:** For editing JavaScript Loops Cheat Sheet type:

```
edit js-loops
```

(opens js-loops.txt)

_Alternatively_ you can also edit the .txt file of a command in a code/text-editor

## How to create a new command?

> **Note:** Creating a new command also creates a new text-file. To edit this new text-file: [click here](#how-to-edit-contents-of-a-cheat-sheet)

```
new-sheet <nameofcommand>       // No White Spaces allowed, use '_', or '-' to separate words
```

**Example:** You want to create a new command / cheat sheet called 'random_notes'

1. Create new command:

```
new-sheet random_notes
```

2. Add content of the new cheat sheet:

```
edit random_notes
```

(opens random_notes.txt)

_Alternatively_ you can also edit the .txt file of a command in a code/text-editor

3. Close and Re-Open Terminal

You can now use 'random_notes' as a new command in your terminal (from any directory) :crab:
