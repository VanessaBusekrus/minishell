#minishell

##Description

minishell is a simplified Unix shell implemented in C as part of the 42 curriculum.
It aims to mimic the behavior of a basic shell, handling command execution, redirections, pipes, environment variables, and built-in commands.

The project focuses on mastering low-level C programming, process management, signal handling, and command parsing.

##Features

* Execute simple commands with arguments
* Handle multiple commands separated by pipes (|)
* Input/output redirection (<, >, >>)
* Built-in commands: `cd`, `echo`, `pwd`, `export`, `unset`, `env`, `exit`
* Support for environment variables
* Signal handling (`Ctrl+C`, `Ctrl+D`)

##Installation

###Clone the repository:

`git clone https://github.com/yourusername/minishell.git
cd minishell`


###Compile the project:

`make`


This will create the minishell executable in the project directory.

##Usage

###Run the shell:

`./minishell`


##Example commands:

`$ echo "Hello, world!"
$ ls -l | grep minishell
$ cat file.txt > output.txt
$ cd ../
$ export MY_VAR="42"
$ echo $MY_VAR
$ exit`

##Built-in Commands

###Command	Description
`cd`	Change the current working directory
`echo`	Display text on the standard output
`pwd`	Print the current working directory
`export`	Set or modify environment variables
`unset`	Remove environment variables
`env`	Display all environment variables
`exit`	Exit the shell


##Implementation Details

* Parsing: Split input into commands, handle quotes and escapes
* Execution: Fork child processes and execute commands
* Redirection: Handle `>,` `>>,` and `<`
* Pipes: Use `pipe()` to connect multiple commands
* Signals: Catch `SIGINT` and `SIGQUIT`
