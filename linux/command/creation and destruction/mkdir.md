The mkdir command in Linux creates new directories (folders). You can run `mkdir Test` to create one in the current directory, or use `mkdir -p` (for example `mkdir -p /home/demo/sub2/Test`) to create parent directories if they don’t already exist.

## Overview of the mkdir Command

The mkdir command in Linux is used to create new directories. It is a fundamental command for organizing files within the file system.

### Basic Usage

- To create a directory in the current working directory, use:
    
    ```
    mkdir directory_name
    ```
    
- For example, to create a directory named "Test":
    
    ```
    mkdir Test
    ```
    

### Creating Directories with Parent Paths

If you want to create a directory along with its parent directories (if they do not exist), you can use the `-p` option:

- Example command:
    
    ```
    mkdir -p /home/demo/sub2/Test
    ```
    

This command will create the "sub2" directory and the "Test" directory within it, creating any necessary parent directories along the way.

### Setting Permissions

You can also specify permissions for the new directory using the `-m` option:

- Example command to create a directory with specific permissions:
    
    ```
    mkdir -m 755 /home/demo/sub1/Test
    ```
    

This sets the permissions to read, write, and execute for the owner, and read and execute for the group and others.

## Summary of Options

|Option|Description|
|---|---|
|`-p`|Create parent directories as needed|
|`-m`|Set permissions for the new directory|
|`directory_name`|Name of the directory to create|

Using the mkdir command effectively allows you to manage your file system structure efficiently.