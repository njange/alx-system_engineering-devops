# Shell Variables and Expansions

This directory contains shell scripts that demonstrate various shell variables and expansions concepts.

## Files Overview

### 0-alias
**Purpose**: Creates a dangerous alias that replaces the `ls` command with `rm *`

**Description**: 
This script demonstrates how to create shell aliases using the `alias` command. When sourced, it creates an alias that maps the `ls` command to `rm *`, which means attempting to list directory contents will instead delete all files in the current directory.

**Usage**:
```bash
source ./0-alias
# or
. ./0-alias
```

**Important Notes**:
- This is a **dangerous** alias intended for educational purposes only
- After sourcing, `ls` will delete all files instead of listing them
- Use `\ls` to bypass the alias and use the original `ls` command
- The alias only affects the current shell session

**Example**:
```bash
$ ls
0-alias  file1  file2
$ source ./0-alias
$ ls
$ \ls
$ 
```

### 1-hello_you
**Purpose**: Prints a greeting message to the current Linux user

**Description**:
This script demonstrates the use of environment variables, specifically the `$USER` variable. It prints "hello" followed by the username of the currently logged-in user.

**Usage**:
```bash
./1-hello_you
```

**Key Concepts**:
- Uses the `$USER` environment variable to get the current username
- Demonstrates variable expansion in shell scripts
- Shows basic `echo` command usage with variables

**Example**:
```bash
$ ./1-hello_you
hello julien
```

## Learning Objectives

These scripts help understand:
1. **Shell Aliases**: How to create command shortcuts and replacements
2. **Environment Variables**: How to access and use system variables like `$USER`
3. **Variable Expansion**: How the shell expands variables in commands
4. **Script Execution**: Different ways to run shell scripts (sourcing vs executing)

## Safety Warning

The `0-alias` script is particularly dangerous as it replaces a commonly used command (`ls`) with a destructive one (`rm *`). Always use caution when working with such aliases and only run them in safe, isolated environments.