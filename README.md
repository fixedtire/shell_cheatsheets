# :shell: Custom Commands for your Console

### short commands to display cheat-sheets in your CLI (executable from any directory)

> [!IMPORTANT]
> The main idea of this project is to help beginner developers improving their workflow. The cheat-sheets are a collection of commands/shortcuts that **_I_** think are useful. If you feel different about it, **you're more than welcome to customize the sheets** (eg. delete/add lines, add custom notes etc). You can also rename the commands, therefor change the alias name ([see here](#installation)).

Available cheat-sheets (customizable):

- CLI-Commands
- GitHub Text Formatting
- JavaScript Conditionals
- JavaScript Loops
- JavaScript Array Methods
- Git/GitHub Commands
- VS Code
- _..maybe your own?_

### :arrow_right: [Directly jump to Installation](#installation)

## Quick-Start

What you'll be able to do with it:

**Example1: For useful CLI-Commands**

_type into console:_

```
showtips
```

example Output:

```
ls                            display files and subdirectories in the directory

cd                            Home directory
cd [folder]                   Change directory, e.g. cd Documents [TAB to suggest]
cd/			      Root of the drive
cd -			      Previous directory or folder you last browsed
pwd			      Show your present working directory

cd ..			      Move up to the parent directory

cd ../..		      Move up two levels

mkdir <dir>		      create new folder named <dir>
mkdir -p <dir>/<dir>	      create nested folders
mkdir <dir1> <dir2> <dir3>	create several folders at once

rm <file>			remove file
rmdir <folder>			remove folder

touch <file>			create a new file without any extension

cat <file>			output the content of <file>

open [file]			opens a file

open . .			opens current directory

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

1. Download .txt files and save it to a directory, example directory: _/Users/mariah/bin/_
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

_Alternative:_ Open configuration with a Text-Editor eg. TextEdit (by default the file islocated in: /Users/yourusername/)

4. Add the following line(s) (you can also cherry-pick depending to your needs :cherries:):

   **Note:** Don't forget to replace the path with the directory where you saved the .txt files!

```
alias gh_format='cat /Users/mariah/bin/github_format.txt'
alias showtips='cat /Users/mariah/bin/terminal_commands.txt'
alias git_commands='cat /Users/mariah/bin/git_commands.txt'
alias vstips='cat /Users/mariah/bin/vs_shortcuts.txt'
alias js-loops='cat /Users/mariah/bin/js-loops.txt'
alias js-array-methods='cat /Users/mariah/bin/js-array-methods.txt'
alias js-conditionals='cat /Users/mariah/bin/js-array-conditionals.txt'
```

5. Save configuration file, close and reopen Terminal
6. You can now use these commands in every directory! :space_invader: :space_invader:
