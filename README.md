# Shell Scripting Tutorial

Shell is a program that allows operating system(OS) to perform actions. Shell scripting allows you to automate `linux terminal tasks` by writing commands in `.sh`file.
## Why use Bash?

Bash is `Bourne Again Shell` which can invoke external programs and have built in commands.

## Syntax of Bash commands

Each Bash command comprises of ***[command] [option] [argument]***

options modify how the command works e.g.,

**ls** (shows content of current working directory)

**ls -a** (some files whose names start with period are hidden and not display by `ls` so `ls -a` is used)

## Some Basic commands

| Commands | Uses | 
|----------|----------|
| ls  | shows contents in current directory    | 
| cd   | takes you to any subdirectory current directory    |   
|cat | uses to see what is inside a file
|mkdir| makes a new empty directory
|sudo| to run commands that requires admin privilege
|rmdir| remove directory
|cp| copies directories and subdirectories
|ps| gives snapshot of all running processes in current directory
|pwd| give path of directory
|touch| create empty file if not exist and if exist updates the timestamp 
|mv| move files

Learning these commands doesn't mean we are done with bash commands, it is just an initial kick, try discovering more commands along with different options like -a,-m,-d etc 

## Steps for Shell Scripting

1. Use **nano filename.sh** to create  a file or open it.
2. Now write commands in such a way that automate tasks such as

     1. folder creation/deletion
     2. backup folder
     3. git operations
     4. software installation etc

3. Here is some  basic shell scripting practice;
 
    1. ```
       echo "Hello, $USER! Welcome to Shell Scripting"
       ```
    2. ```
        if [ "$name" = "Ali" ]; then
          echo "Hi Ali!"
        fi
        ```
    3. ```
       for i in 1 2 3; do echo $i; done
       ``` 
    4. ```
       #!/bin/bash
       # backing up a folder
       SOURCE_FOLDER="/path/to/your/folder"
       BACKUP_FOLDER="/path/to/backup/location"

       if [ -d "$SOURCE_FOLDER" ]; then
           echo "Source folder exists. Starting backup..."
           mkdir -p "$BACKUP_FOLDER"
           cp -r "$SOURCE_FOLDER" "$BACKUP_FOLDER"
           echo "Backup completed successfully!"
       else
          echo "Source folder does not exist. Backup failed."
       fi
         ```

4. After writing the script save the file and in the terminal type `chmod +x filename.sh` to make it executable and then type `./filename.sh` to run it

## Evaluate yourself

Try writing a script that checks if a folder exists, and if not, it creates it automatically!






