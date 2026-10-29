rm (short for “remove”) is the Linux command used to delete files from the file system, and by default it does not delete directories. Use -r to remove directories recursively (along with everything inside)

## Overview of the `rm` Command in Linux

The `rm` command, short for "remove," is a fundamental command in Linux used to delete files from the file system. It is important to use this command with caution, as it does not provide a way to recover deleted files.

### Basic Usage

- Syntax:
    
    ```
    rm [OPTION] [FILE]
    ```
    
- Default Behavior:
    
    - By default, `rm` deletes specified files but does not delete directories.

### Common Options

|Option|Description|
|---|---|
|`-r`|Recursively delete directories and their contents.|
|`-i`|Prompt for confirmation before each file deletion.|
|`-f`|Force deletion without prompting for confirmation.|

### Examples

- To delete a single file:
    
    ```
    rm filename.txt
    ```
    
- To delete a directory and all its contents:
    
    ```
    rm -r directory_name
    ```
    
- To delete multiple files with confirmation:
    
    ```
    rm -i file1.txt file2.txt
    ```
    

### Important Considerations

- Irrecoverable Deletion: Files deleted using `rm` do not go to a recycle bin; they are permanently removed.
- Safety Practices: It is advisable to use the `-i` option or create aliases to prevent accidental deletions. For example:
    
    ```
    alias rm="rm -i"
    ```
    

Using the `rm` command effectively requires understanding its options and the implications of file deletion. Always double-check the files or directories you intend to remove to avoid unintended data loss.