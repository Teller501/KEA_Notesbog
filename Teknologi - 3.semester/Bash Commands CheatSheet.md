# Bash Command Cheatsheet

## cd

**Syntax**: `cd [directory]`

Change the current working directory to the specified directory. If no directory is specified, change to the home directory.

## ls

**Syntax**: `ls [options] [files]`

List directory contents. Common options:

- `-l` - Use a long listing format
- `-a` - Show hidden files 
- `-R` - List subdirectories recursively

## mkdir 

**Syntax**: `mkdir [options] <directory>`

Create a new directory. Common options:

- `-p` - Create parent directories as needed

## rm

**Syntax**: `rm [options] <files>` 

Remove (delete) files or directories. Common options:

- `-r` - Remove directories and their contents recursively
- `-f` - Force removal without prompting for confirmation

## cp

**Syntax**: `cp [options] <source> <destination>`

Copy files and directories. Common options:

- `-R` - Copy directories recursively
- `-i` - Prompt before overwriting existing files

## mv

**Syntax**: `mv [options] <source> <destination>` 

Move or rename files and directories.

## cat

**Syntax**: `cat [options] <files>`

Display file contents to standard output. Common options: 

- `-n` - Number all output lines

## grep 

**Syntax**: `grep [options] <pattern> <files>`

Search files for lines matching a pattern. Common options:

- `-i` - Perform case-insensitive matching
- `-R` - Recursively search subdirectories

## pwd

**Syntax**: `pwd`

Print the current working directory. 

## echo

**Syntax**: `echo [options] <string>`

Display a string of text. Common options:

- `-n` - Do not print a newline after the text
