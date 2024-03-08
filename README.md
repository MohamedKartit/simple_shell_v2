# Simple Shell
this simple shell mimics bash shell.

## Description 
Custom version UNIX command language interpreter. This mini shell reads commands from either interactive mode and non-interactive mode.

## Quick start
Git clone the repository:
```
https://github.com/MohamedKartit/simple_shell_v2.git
```

## Usage
All the files are to be compiled on an Ubuntu 14.04 LTS machine with:
```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
```

Once compiled, to start the program, run:
```./hsh```
  
To exit the program, run:
```$ exit```
  
it supports most shell commands, such as ```cat```, ```pwd```, ```ls -la``` and more.

## Syntax
the user can have the experience in an interactive and non-interactive way. On the one hand, if it is invoked with a standard input that is not connected to the terminal,it reads and executes the received commands in order.

To use the program interactive mode use isatty(3). Immediately the user will see a warning ```$``` indicating that our shell is ready to read the command.

On the other hand, in non-interactive mode the user will enter command line arguments, so the shell  treats the first argument as a file from which to read the commands.
In interactive mode, you can type commands from the keyboard:

Example:
```
$ ./hsh
$ /bin/ls
```
In non-interactive mode, you can pipe commands into the program using echo or cat:

Non-interactive:

Example:
```
$ echo "/bin/ls" | ./hsh
$ cat file_name | ./hsh
```

You can use the same syntax for running commands in other shells:
```
<command> <flags or options> <argument 1> <argument 2> ...
```

In non-interactive mode:
```
<command> | ./hsh
```

## Built-Ins
The following built-ins are supported by the program:
  
+ ```env``` - Print the current environment
+ ```exit``` - exit program sucessfully

## Return
the program returns zero indicating success and non-zero indicanting failure.
