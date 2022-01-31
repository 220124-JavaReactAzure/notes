# Unix/Linux

## Commands

-   Before we begin with commands

    -   we should cover the basic aliases for locations in your file system.
    -   A **file system**

        -   is generally comprised of a directory(folder) that itself can contain files and directories in a tree structure
        -   The top-level directory is known as the root directory and it is the folder that contains all of the other folders on the drive partition you are currently accessing
        -   In **Unix** your root directory is represented by the / character

            -   if you wished to change directory to the root directory from anywhere on the partition, you would issue the following command:

            ```bash
            cd /
            ```

-   That's all well and good, but what about the directory you're currently in?

    -   **.** character represents the current directory
    -   **..** represents the parent directory

        ```bash
        # Copies all the current directory files up            one directory
        cp -r . ..
        ```

-   In Unix we also have a directory called the **home directory**
    -   This directory is represented by the ~ character
    -   This directory is usually the one that our terminal starts in and it is where our personal files are generally stored.

## Arguments and Flags

-   **_Arguments_**
    -   given to a command take the form of strings written after the command
        -   ex. command arg1 arg2 arg3
    -   usually represent variables or targets for your command
-   **_Flags_**

    -   usually represent options you wish to enable for your command
    -   are special arguments given to a command.
    -   There are two kinds of flags in Unix,

        -   **short-hand** or **character flags**
            -   a single character (or group of characters) prefixed by a single dash -c
        -   **full flags**
            -   the full name of the flag prefixed by a double dash --flag.

        ```bash
        # This command performs the exact same action
        cp -r . ..
        cp --recursive . ..
        ```

## The Most Important Command

-   **man**
    -   The manual command will print to the terminal the manual for using a particular command.
    -   If you are unsure what flags or arguments a command takes
        -   simply type man command

```bash
# Prints out the manual for cp to the terminal windodw
man cp
```

### Directory Commands

```bash
#### cd command ####
# cd - The change directory command allows us to navigate to a different directory on the drive.
# go to root directory:
cd /
#go to home directory:
cd or cd ~
# navigate one directory up:
cd ..
#navigate into the hi directory, which is inside the bye directory:
cd ./bye/hi
#change to the previous directory:
cd -

#### ls command ####
# ls - The list directory command allows us to see the contents of a particular directory. When given no arguments, it lists the contents of the current directory. The -a flag allows you to see hidden items in the directory.
#list the contents of the current directory:
ls
#list the contents of the hi directory:
ls hi or ls ./hi
#list the contents of the directory including the "hidden" contents:
ls -a

#### mkdir command ####
# mkdir - The make directory command allows us to create a new directory. mkdir takes an argument representing the name of the directory you wish to create.
#create a directory named hi:
mkdir hi

#creates the parent directories if they don't exist

#pwd - The print working directory command prints the full name of the directory you are currently working in. For example, if you were working in the home directory inside of the root directory the output of pwd might be /home.
#Prints out the current working directory
pwd

```

### General Purpose Commands

```bash

# the sudo command allows you to run a particular command as the root user.
sudo
# the clear command usually prints a number of blank lines such that all previous commands are no longer on the screen. There is a shortcut for this command, ctrl-l
clear
# the echo command will print a string or the result of a command to the console.
echo
# The > operator will redirect the output of a command to a file. The file will be created or overwritten if it already exists. ex.
ls . > log.txt

# The >> operator acts the same way as the > operator but appends output to the file instead of overwriting if it exists.
ls ./sub-directory >> log.txt

# the grep command prints any lines in a file or files that match a given pattern. By default, grep interprets the pattern as a basic regular expression.
# match all lines that start are 0-9
grep "*[0-9]" log.txt

# Print all lines in hello.txt that contain the word goodbye:
grep goodbye hello.txt
```

### File Commands

```bash
#cat command the concatenate command prints the contents of a file to the console.
cat hello.txt
#head command prints the first ten lines of a file to the console.
head hello.txt
#tail command prints the last ten lines of a file to the console.
tail hello.txt
#touch command allows you to modify the timestamp of a file. This command is usually used to #create empty files, as an empty file is created if touch is given a file name that does not exist.
touch hello.txt
#cp command(copy) creates a copy of the specified file at the location specified. If the recursive glag is used, it will operate on directories.
#copy a hello.txt to goodbye.txt:
cp hello.txt goodby.txt
#copy the hello directory to the goodbye directory:
cp -r hello goodbye
# mv commands can be DANGEROUS as it overwrites with no way to undo that overwrite. Prefer the us of cp above until comfortable with command line
# mv command(move) will rename or move a file or entire directory with the recursive flag.
# rename a hello.txt to goodbye.txt:
mv hello.txt goodbye.txt
# move hello.txt to the goodbye directory:
mv hello.txt goodbye/.
# rename the hello directory to goodbye:
mv -r hello goodbye
# rm command(remove) will delete a file. If you use the recursive flag, it can delete a directory. The force flag will cause the command to delete files without prompting the user if there are warnings. # THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# remove hello.txt:
rm hello.txt
# remove the hello directory:
rm -r hello
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# THE COMMAND rm -rf . is EXTREMELY DANGEROUS
# wc command(word count) will print the number of words in a file. This command has several flags available
#    -c, --bytes - prints the byte count
#    -m, --chars - prints the character count
#    -l, --lines - prints the lines
#    -w, --words - prints the word count (default)
# ln command(link) creates a link between files. This allows you to make a shortcut to a file in one location without copying it over.
```
