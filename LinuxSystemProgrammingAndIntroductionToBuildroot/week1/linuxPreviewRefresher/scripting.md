# Scripting
- Scripting allows us to
    - automate frequently used commands
    - customize commands for different scenarios using arguments and variables
- think of scripts as documentation
    - if you find yourself listing commands used to perform a task, consider scripting instead
- often ends with .sh (short for shell)
    
## Example
- #!/bin/sh is a comment which tells the shell which shell interpreter to use. It as also known as *shebang*
- also common to see #!/bin/bash

## Script Variables
- Script variables include:
    - varibles we define ourselves
    ```bash
    #!/bin/bash
    greeting=hello
    echo "${greeting} world"
    ```
    - Variables passed into script arguments 
    ```bash
    #!/bin/bash
    greeting=$1 
    echo "${greeting} world"
    ```
    run:
    ```bash
    $ ./helloworldargs.sh hola 
    $ hola world
    ```
## Script arguments
- Script special chars
    - $0 : the invoked name of the bash script
    - $1 - $9 : first 9 args to script
    - $# : number of args passed to the script
    - $? : the exit status of the most recent process
