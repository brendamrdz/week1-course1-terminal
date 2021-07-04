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
| ls       | List of files in the current working directory                                                                                                                 | ls                                      |
| cd       | To navigate through the Linux files and directories                                                                                                         | cd /[path-directory]             |
| clear    | Clean the terminal from past commands.                                                                                                                      | clear                                   |
| pwd      | Print working directory path.                                                                                                                               | pwd                                     |
| tree     | Displays the directory structure in a drive graphically.  Add -l flag to specify the levels of the tree.                                                    | tree -l2                                |
| mkdir    | Creates a new directory.                                                                                                                                    | mkdir dirname1                          |
| touch    | Creates a new file.                                                                                                                                         | touch filename.ext                      |
| cp       | Copy files from the current directory to a different directory.                                                                                             | cp filename.ext /home/username/new-path |
| mv       | Move files from the current directory to a different directory also used to rename files.                                                               | mv filename.ext /home/username/new-path. |
| rm       | Deletes files.                                                                                                                                              | rm filename.ext                         |
| head     | Displays the first lines of any text file. By default, it will show the first ten lines. To modify the number of lines add -n.| head -n 5 filename.ext.                 |
| tail     | Displays the last lines of any text file. By default, it will show the first ten lines. To modify the number of lines add -n.| tail -n 20 filename.ext.                 |
| Less     | Displays all the content of a file.                                                                                                                          | less filename.ext                       |
| type     |    It will show you how a given command would be interpreted if typed on the command line.                                                                                                                                                         | type command                            |
| alias    | The alias command is used to convert any Linux command into it's own command and keyword.                                                                                                                                                            |     alias www='ll /var/www/'                                    |
| --help   | Helps display brief summaries of shell builtin commands.                                                                                                                                                            | echo --help                      |
| man      | Displays the user manual for a command .                                                                                                                     | man commandname                         |



## Wildcards
Commands can use wildcards to perform actions on more than one file at a time.

|    | Here is the basic set of wildcards: |
|----|-------------------------------------|
| *  | represents zero or more characters  |
| ?  | represents a single character       |
| [] | represents a range of characters    |

### Examples

Displays all those files that have the word data in the file name.

```bash
ls data*
```
Displays all those files that have the word data and end with a characters in the file name.

```bash
ls datos?
```
Displays all those directories that start with lowercase and uppercase
```bash
ls -d [[:upper:]] 
```
```bash
ls -d[[:lower:]] 
```
## Network Utilities

| Command    | Description                                                                                                     |
|------------|-----------------------------------------------------------------------------------------------------------------|
| ifconfig   | Displays network information.                                                                                     |
| ping       | It’s a way to see whether a computer can communicate with the Internet or a specific IP address.                |
| curl       | Downloads a file from the Internet without leaving the terminal. Type curl -O followed by the path to the file. |
| wget       | Downloads a file from the Internet without leaving the terminal.                                                |
| traceroute | Prints the route that a packet takes to reach the host.                                                         |
| netstat -i | Displays network devices.                                                                                        |                                             |

## How does the shell works
![how does the shell works](https://github.com/brendamrdz/week1-course1-terminal/blob/main/images/Picture1.png?raw=true)
### Pipe operator
The pipe character redirects the standard output from one command to the standard input of another command. 
```bash
ls -lh | less
```
### Redirecting Standard Output
The greater-than (>) metacharacter directs the standard output to a file instead of printing the output to the screen.
```bash
ls Pictures > myPictures.txt
```
### Redirecting Standard Error
A command using the file descriptor number (2) and the greater-than (>) sign redirects any standard error messages to the /dev/null file.
```bash
less file.tst 2> /dev/null
```
## Control Operators
| Control Operator              | Usage                                                                                                                                    | Syntax                     |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| ;semicolon                    | Semicolon is used for separation of two or more commands on a single line of command prompt.                                              | echo Hello ; echo World    |
| & ampersand                   | The execution of command takes place in the background of the command prompt. It shows full result after completion of full process in the background. | echo Hello World &         |
| && double ampersand           | In this case this operator checks if the first condition is true then only the second will execute.                                           | echo Hello && echo World   |
| || double vertical bar      | Double vertical bar is used as OR logical operators that check two commands. In this case the operator check both conditions.            | echo Hello || echo World |
## How to manage permissions
The permissions control the actions that can be performed on the file or directory. They either permit, or prevent, a file from being read, modified or, if it is a script or program, executed. 
* chmod command modifies Linux file permissions

Types of mode
- Owner
- Group
- World

| SYMBOLIC MODE | TYPES OF MODES     |
|---------------|-----------|
| u             | user      |
| e             | group     |
| o             | world     |
| a             | all modes |

|     TYPES OF MODES    |                |                                                     |
|-----------------------|----------------|-----------------------------------------------------|
|     OCTAL             |     BINARIO    |     PERMISSIONS rwx  (read,   write,    execute)    |
|     0                 |     000        |     ---                                             |
|     1                 |     001        |     --x                                             |
|     2                 |     010        |     -w-                                             |
|     3                 |     011        |     -wx                                             |
|     4                 |     100        |     r--                                             |
|     5                 |     101        |     r-x                                             |
|     6                 |     110        |     rw-                                             |
|     7                 |     111        |     rwx                                             |

### Change permissions example
Remove permission from a user to read
```bash
chmod u-r nameFile.txt
```
Add read permission for a user to read
```bash
chmod u+r nameFile.txt
```

