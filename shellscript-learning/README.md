# Shell Script Learning

## Commands

`ls` show file and directories in current path

`man` help command ex: `man ls`

`touch` for create a new file.

`vim`, `vi`, `nano` for text editor.

`cat` show text file

`chmod` change permission of file

    chmod [owner][group][everyone]

    1: execute
    2: write
    4: read

    we can sum the numbers to set multiple permission for example

    chmod 775 bash.sh => give all permission to owner and group and just read and execute to everyone for 'bash.sh' file

`history` all command history

`pwd` current path directory

`mkdir` create directory

`clear` clear terminal

`cd` change directory

    .  => current path
    .. => previous path

`df` show available and used space

`free` show the memory of the machine

`nproc` number of cpu

`pc` running processors

`ps -ef` running processors with users

`grep` filter the result of the commands

    ps -ef | grep "root"

`date` current date time

`awk` process the text. example: `ps -ef | awk -F " " '{print $1}'`

`wget` download file

`curl` http request

`find` search a file

`kill` kill a process

## Bash script

shebang : `#!/`
    - `#!/bin/bash` (common)
    - `#!/bin/sh`
    - `#!/bin/ksh`
    - `#!/bin/dash`

`set -x` debug mode. show the commands that execute in script.

```sh
set -e # exit the script when there is an error
set -o pipefail
```

### Condition

```sh
if [expression]
then
    # do some tings
else
    # do some thing too
fi
```

for example :

```sh
a=10
b=20

if [$a > $b]
then
    echo "a is bigger"
else
    echo "b is bigger"
if
```

### Iteration

```sh
for i in {1.100} do echo $1; done
```
