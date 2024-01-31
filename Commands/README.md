# Linux Besic Commands

The Linux command is a utility of the Linux operating system. All basic and advanced tasks can be done by executing commands. The commands are executed on the **Linux terminal**. The terminal is a command-line interface to interact with the system, which is similar to the command prompt in the Windows OS. Commands in Linux are **case-sensitive**.

Linux terminal is a user-friendly terminal as it provides various support options. To open the Linux terminal, press `CTRL + ALT + T` keys together, and execute a command by pressing the `ENTER` key.

In this topic, we will discuss some most frequently used Linux commands with their examples. These commands are very useful for a beginner and professional both. We have divided these commands into following sections so that you can easily identify their usage:

- [Linux Directory Commands](https://github.com/rakibulhasanimran/Linux/blob/main/Command/README.md#linux-directory-commands)
- [Linux File Commands](https://github.com/rakibulhasanimran/Linux/blob/main/Command/README.md#linux-file-commands)
- Linux File Content Commands
- Linux User Commands
- Linux Filter Commands
- Linux Utility Commands
- Linux Networking Command

### Linux Directory Commands
**1. `pwd` Command:** The `pwd` command in Linux stands for "print working directory." It is used to display the current working directory, which is the directory in the file system where a user is currently located.

*Syntax:*
```bash
pwd
```

*Example:*
```bash
pwd
```

This command will print the full path of the current working directory to the terminal.

The `pwd` command is useful when you want to know your current location in the file system, especially if you are navigating between directories and need to confirm your present working directory.


**2. `mkdir` Command:** The `mkdir` command is used to create a new directory under any directory.  It stands for "make directory."

*Syntax:*
```bash
mkdir [options] <directory_name>
```

- `[options]`: Additional parameters to customize the behavior of the mkdir command.
- `<directory_name>`: The name of the directory to be created.

*Example:*
```bash
mkdir new_directory
```

In this example, the `mkdir` command is used to create a new directory named "new_directory" in the current working directory. You can replace "new_directory" with the desired name of the directory you want to create.

The `mkdir` command in Linux has a few options to customize its behavior. Here are the common options:

- `-m`, `--mode=MODE`: Set the file permission bits for the newly created directory. The mode is specified in octal representation. *For example:*
```bash
mkdir -m 755 new_directory
```
- `-p`, `--parents`: Create parent directories as needed. If a parent directory in the given path does not exist, it will be created. *For example:*
```bash
mkdir -p parent_directory/new_directory
```
- `--help`: Display help information about the mkdir command.
- `--version`: Display the version information of the mkdir command.

These options allow users to set permissions, create parent directories, and access information about the `mkdir` command. You can use them individually or combine them as needed.
    

**3. `rmdir` Command:** The `rmdir` command is used to delete a directory. It stands for "remove directory."

*Syntax:*
```bash
rmdir [options] <directory_name>
```

- `[options]`: Additional parameters to customize the behavior of the `rmdir` command.
- `<directory_name>`: The name of the directory to be removed.

*Example:*
```bash
rmdir empty_directory
```

In this example, the `rmdir` command is used to remove the directory named "empty_directory" from the current working directory. It's important to note that the directory must be empty for `rmdir` to successfully remove it.

The rmdir command in Linux is relatively straightforward and doesn't have many options. It is primarily used to remove empty directories. Here's the one common option:

- `--ignore-fail-on-non-empty`: Ignore failure when attempting to remove a non-empty directory. This option allows `rmdir` to proceed with the removal even if the specified directory is not empty. *For example:*
```bash
rmdir --ignore-fail-on-non-empty  non_empty_directory
```

> Please note that the `--ignore-fail-on-non-empty` option is not available in all versions of the `rmdir` command. Depending on your system, you may need to check the available options using the command `rmdir --help` or `man rmdir` for more detailed information.



**4. `ls` Command:** The `ls` command is used to display a list of content of a directory.

*Syntax:*
```bash
ls [options] [files or directories]
```

- `[options]`: Additional parameters to customize the behavior of the `ls` command.
- `[files or directories]`: Optional arguments to specify which files or directories to list. If not provided, it lists the contents of the current directory.

The command can be enhanced by incorporating options for a more tailored display:

*Example:*
```bash
ls
```
This command will list the contents of the current directory.

The available options of the `ls` command include:

- `-l`: Display detailed information about files and directories.
    
- `-a`: List all entries, including hidden files.
- `-h`: Provide human-readable file sizes.
- `-R`: Recursively list subdirectories.
- `-t`: Sort files by modification time.
- `-S`: Sort files by size.
- `-r`: Reverse the order of the sort.
- `-u`: Display files by access time.
- `-d`: List directories themselves, not their contents.
- `--color`: Colorize the output for better visual distinction.
- `-1`: Display each entry on a new line.

These options enable users to customize the appearance and details of the directory listing based on their specific requirements. You can use them individually or combine them as needed.

**5. `cd` Command:** The `cd` command is used to change the current directory.

*Syntax:*
```bash
cd <directory_name>
```

- `<directory_name>`: The directory to change into. If not specified, the command will switch to the user's home directory by default.

*Examples:*
```bash
cd /path/to/directory   # Change to a specific directory
cd                      # Change to the user's home directory
cd ..                   # Move up one level in the directory hierarchy
cd ~                    # Shortcut to the user's home directory
cd -                    # Switch to the previous directory
```

The `cd` command is fundamental for navigating the file system in the command-line interface, allowing users to move between directories and access different parts of the file system.

### Linux File Commands

**1. `touch` Command:** The `touch` command in Linux is used to create empty files or update the access and modification times of existing files.

*Syntax:*
```bash
touch [options] <file_name>
```

- `[options]`: Additional parameters to customize the behavior of the `touch` command.
- `<filename>`: The name of the file to be created or modified.

*Example:*
```bash
touch new_file.txt
```

In this example, the touch command is used to create a new empty file named "new_file.txt" in the current working directory.

We can create multiple empty files by executing it once.

*Syntax:*
```bash
touch <file1>  <file2> ....  
```

Common options:
- `-c`: Do not create a new file if it does not exist. This option prevents the creation of a new file if the specified file is not found.*For example:*
```bash
touch new_file.txt
```

The touch command is versatile and is frequently used in scripts or commands where the existence or modification time of a file needs to be updated.


**2. `cat` Command:** The `cat` command in Linux is used to concatenate and display the content of files. It can also be used to create new files, concatenate files, and display the contents of files on the terminal.

*Syntax:*
```bash
cat [options] [file(s)]
```

- `[options]`: Additional parameters to customize the behavior of the cat command.
- `[file(s)]`: The file or files whose contents are to be displayed or concatenated.

*Examples:*
```bash
cat filename          # Display the content of a file
cat file1 file2       # Concatenate the contents of multiple files
```

Common options:
- `-n`: Number all output lines, displaying line numbers.
- `-A`: Display all characters, including non-printing characters, and show line endings with special characters.

To create a file, execute it as follows:

*Syntax:*
```bash
cat > <file_name>  
// Enter file content  
```

Press "CTRL+ D" keys to save the file. To display the content of the file, execute it as follows:

*Syntax:*
```bash
cat <file_name>  
```

The `cat` command is a versatile tool for viewing and manipulating file content in the command line. It is widely used in various shell scripts and commands for file-related operations.


**3. `rm` Command:** The `rm` command in Linux is used to remove or delete files and directories.

*Syntax:*
```bash
rm [options] <file(s) or directory(s)> 
```

- `[options]`: Additional parameters to customize the behavior of the rm command.
- `<file(s) or directory(s)>`: The file or directory names to be removed.

*Examples:*
```bash
rm file.txt          # Remove a single file
rm -r directory      # Remove a directory and its contents recursively 
```

Common options:
- `-f`: Forcefully remove files or directories without prompting for confirmation.
- `-i`: Interactively prompt the user before removing each file.
- `-r`: Remove a directory and its contents recursively.

It's crucial to use the `rm` command with caution, especially with the `-r` (recursive) and `-f` (force) options, as it can lead to the permanent deletion of files and directories. Always double-check your command and ensure that you are removing the intended files.

**4. `cp` Command:** The cp command in Linux is used to copy files and directories from one location to another.

*Syntax:*
```bash
cp [options] <source> <destination>
```

- `[options]`: Additional parameters to customize the behavior of the `cp` command.
- `<source>`: The file or directory to be copied.
- `<destination>`: The location where the copy will be placed.

*Examples:*
```bash
cp file.txt /path/to/destination     # Copy a file to a specified location
cp -r directory /path/to/destination # Copy a directory and its contents recursively
```

Common options:
- `-r`: Copy directories recursively. This option is necessary when copying directories.
- `-i`: Interactive mode. Prompt before overwriting existing files.


**5. `mv` Command:** The `mv` command in Linux is used to move or rename files and directories. It is a versatile command that allows for various file and directory operations.

*Syntax:*
```bash
mv [options] <source> <destination>
```

- `[options]`: Additional parameters to customize the behavior of the mv command.
- `<source>`: The file or directory to be moved or renamed.
- `<destination>`: The location where the source will be moved or the new name if renaming.


*Examples:*
```bash
mv file.txt /path/to/destination     # Move a file to a specified location
mv oldfile.txt newfile.txt            # Rename a file
mv directory /path/to/destination    # Move a directory to a specified location
```

Common options:
- `-i`: Interactive mode. Prompt before overwriting existing files.
- `-u`: Update. Move only when the source file is newer or the destination file is missing.

The `mv` command is crucial for managing file and directory locations as well as renaming. Be cautious, especially when moving or renaming files, to prevent unintentional data loss or overwrites.


### Linux File Content Commands
### Linux User Commands
### Linux Filter Commands
### Linux Utility Commands
### Linux Networking Command
