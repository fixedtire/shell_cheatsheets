# :shell: Shell Cheat-Sheets

_Note: So far this is only for MAC Users (Bash/ZShell)_

### :arrow_right: [Directly jump to Installation](#installation)

## Quick-Start

What you'll be able to do:

_example1_

```
showtips
```

displays to console:

```
ls                      display files and subdirectories in the directory

cd                      Home directory
ls                      display files and subdirectories in the directory
cd [folder]             Change directory, e.g. cd Documents [TAB to suggest]
cd/				Root of the drive
cd -				Previous directory or folder you last browsed
pwd				Show your present working directory

cd ..				Move up to the parent directory

cd ../..			Move up two levels

mkdir <dir>			create new folder named <dir>
mkdir -p <dir>/<dir>		create nested folders
mkdir <dir1> <dir2> <dir3>	create several folders at once

rm <file>			remove file
rmdir <folder>			remove folder

touch <file>			create a new file without any extension

cat <file>			output the content of <file>

open [file]			opens a file

open . .			opens current directory

// list goes on
```

_example2_ syntax to format github text files

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

1. Download .txt files and save it to a directory, example directory: _/Users/mariah/bin/_
2. Figure out if you are using ZShell or Bash:

```
echo $SHELL
```

3. Open your Configuration File:

a: For ZShell type:

```
 nano ~/.zshrc
```

b: For Bash type:

```
 nano ~/.bshrc
```

_Help for GNU:_ [CMD] + [X] to save, press [Y] to save, [ENTER] to confirm

_Alternative:_ Open the configuration with TextEdit (by default located in: /Users/yourusername/)

4. Add the following line(s) (you can also cherry-pick depending to your needs :cherries:):

   **Note:**Don't forget to replace the path with the directory where you saved the .txt files!

```
alias gh_format='cat /Users/mariah/bin/github_format.txt'
alias showtips='cat /Users/mariah/bin/terminal_commands.txt'
alias git_commands='cat /Users/mariah/bin/git_commands.txt'
```

5. Save configuration file, close and reopen Terminal
6. You can now use these commands in every directory! :space_invader: :space_invader:
