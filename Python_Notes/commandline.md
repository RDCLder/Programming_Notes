# The Command Line

## Mac: Command Line

- OS File Structure
  - Directories are organized in a tree hierarchy with parents and children that all branch off from the **root** directory.
  - **Root** directory
    - Path:  root/
    - Files and directories have absolute paths based on the root directory.
    - Each additional level down is denoted by a backslash /
  - **Home** directory  
    - Path:  root/Users/username
    - Terminals open in the **home** directory by default.
    - The home directory can be accessed by typing cd ~
    

---

## Windows: PowerShell

-	The PowerShell is the command line equivalent for windows OS
  - An OS is structured like a tree in which a root directory can then branch off into subdirectories (e.g. folders, files, etc.)
    - Root directory is C:
    - Levels of the hierarchy are separated by \
    - Home directory is designated by ~ and is usually C:\Users\Username

  - The command line has greater functionality than a GUI like Windows Explorer or Mac Finder
    - There are special keywords that can perform the same functions as a GUI and much more.
    - e.g.  Instead of manually dragging a file from directory to directory, PowerShell can perform that function with a line of code.
  
  - Command Line Uses
    - Navigate around directories
    - Create and remove directories and files
    - Move, copy, and paste things
    - Execute scripts

-	PowerShell has several basic functions that can be used to manipulate files
  - Basic directory functions
    - cd  addresses the current directory
    - ..	goes back one level to parent directory (e.g. cd ..)
    - ls	lists all the contents of current directory
    - wpd	lists the exact path from root directory to current directory
    - ~	accesses the home directory

  - Other functions
    - clear	clears current PowerShell text

- Creating Directories
  - mkdir command can make new directories
    - syntax:  mkdir folder
    - This will create a new folder called “folder” in the current directory

---
