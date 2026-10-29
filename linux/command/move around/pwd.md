pwd (print working directory) in Linux prints the full path of your current working directory to the terminal (standard output). Use -L for the logical path using the PWD environment variable, or -P for the physical path with symbolic links resolved.

## Overview of the pwd Command in Linux

The pwd command stands for "print working directory." It is used in Linux to display the full path of the current working directory in the terminal.

### Basic Functionality

- Purpose: Prints the absolute path of the current directory.
- Output: The command outputs the path starting from the root directory (/) to your current location.

### Command Syntax

bash

```
pwd [OPTION]
```

### Options Available

|Option|Description|
|---|---|
|-L|Displays the logical path using the PWD environment variable.|
|-P|Displays the physical path, resolving any symbolic links.|

### Example Usage

1. To display the current directory:
    
    bash
    
    ```
    pwd
    ```
    
    Output might look like:
    
    ```
    /home/user/Documents
    ```
    
2. Using the -L option:
    
    bash
    
    ```
    pwd -L
    ```
    
    This shows the logical path, which may include symbolic links.
    
3. Using the -P option:
    
    bash
    
    ```
    pwd -P
    ```
    
    This shows the physical path, ignoring symbolic links.
    

### Practical Applications

- Scripting: You can store the current directory in a variable for use in scripts:
    
    bash
    
    ```
    current_dir=$(pwd)echo "The script is running in: $current_dir"
    ```
    

The pwd command is essential for navigating and managing files within the Linux filesystem, especially in complex directory structures.