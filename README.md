# Introduction to the Terminal and Command Line

## General info

The aim of this project is to summarize the content of the course "Introduction to the Terminal and Command Line". Here you can find the most common commands used in the command line.

## What is a terminal?
This is a program that opens a window and lets you interact with the shell.

## Command line (Shell)
The shell is a program that takes commands from the keyboard and gives them to the operating system to perform.

### Types of Shells
- Bourne Shell
- Bash Shell
- Z Shell
- C Shell
- Korn Shell
- Fish Shell
- Power Shell

## Command
A program that can be execute from the terminal. It could recibe parameters and options.

| Commands | Description                                                                                                                                                 | Syntax                                  |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| ls       | List files in the current working directory                                                                                                                 | ls                                      |
| cd       | To navigate through the Linux files and directories                                                                                                         | cd /home/username/Downloads             |
| clear    | Clean the terminal from past commands.                                                                                                                      | clear                                   |
| pwd      | Print working directory path.                                                                                                                               | pwd                                     |
| tree     | Displays the directory structure in a drive graphically.  Add -l flag to specify the levels of the tree.                                                    | tree -l2                                |
| mkdir    | Creates a new directory.                                                                                                                                    | mkdir dirname1                          |
| touch    | Creates a new file.                                                                                                                                         | touch filename.ext                      |
| cp       | Copy files from the current directory to a different directory.                                                                                             | cp filename.ext /home/username/new-path |
| mv       | Move files from the current directory to a different directory also It works to rename files.                                                               | mv filename.ext /home/username/new-path |
| rm       | deletes files.                                                                                                                                              | rm filename.ext                         |
| head     | Displays the first lines of any text file. By default, it will show the first ten lines. To modify the number of lines add -n flag and the number of lines. | head -n 5 filename.ext.                 |
| tail     | Displays the last lines of any text file. By default, it will show the first ten lines. To modify the number of lines add -n flag and the number of lines.  | tail -n 20 filename.ext                 |
| Less     | Displays all the content of a file                                                                                                                          | less filename.ext                       |
| type     |                                                                                                                                                             | type command                            |
| alias    |                                                                                                                                                             |                                         |
| --help   |                                                                                                                                                             | commandname --help                      |
| man      | Displays the user manual for a command                                                                                                                      | man commandname                         |
| info     |                                                                                                                                                             |                                         |
| whatis   | a                                                                                                                                                           |                                         |


## Wildcards
Commands can use wildcards to perform actions on more than one file at a time.

|    | Here is the basic set of wildcards: |
|----|-------------------------------------|
| *  | represents zero or more characters  |
| ?  | represents a single character       |
| [] | represents a range of characters    |

### Examples

Displays all those files that have the word data in the file name

```bash
ls data*
```
Displays all those files that have the word data and ends with a characters in the file name

```bash
ls datos?
```
Displays all those directorys that start with lowercase and uppercase
```bash
ls -d [[:upper:]] 
```
```bash
ls -d[[:lower:]] 
```
