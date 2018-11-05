# The Command Line

## Mac Terminal

- Command Line Uses
  - Navigate around directories
  - Create and remove directories and files
  - Move, copy, and paste things
  - Execute scripts
  - Perform all the functions of a traditional GUI (e.g. Windows Explorer or Mac Finder) and more

- OS File Structure
  - Directories are organized in a tree hierarchy with parents and children that all branch off from the **root** directory.
  - **Root** directory
    - Path:  ```root/```
    - Files and directories have absolute paths based on the root directory.
    - Each additional level down is denoted by ```/```
  - **Home** directory  
    - Path:  ```root/Users/username```
    - Terminals open in the **home** directory by default.
    - The home directory can be accessed with ```cd ~```

- Commands and Options
  - Commands have options that can modify their behavior.  Options can be used separately or together.
  - **clear**:  Clears the terminal history.
  - **pwd**:  "Print Working Directory".  Prints the path of the current directory.
  - **ls**:  "List".  Lists all files and folders in the current directory.
    - ```ls -a``` lists all contents including hidden files and directories that start with ```.```
    - ```ls -l``` lists all contents in long format.  From left to right, they correspond to the following:
      - Access rights.  Actions permitted on the files and directories contained.
      - Number of hard links.  Number of child directories and files contained.
      - Name of user that owns file/directory.
      - Name of group that owns file/directory
      - File size
      - Date and time last modified.
      - Name of file/directory.
    - ```ls -t``` lists all contents in order of time created.
  - **cd**:  "Change Directory".  Changes the working directory to a specified directory.
    - The specified directory must either be directly accessible from the working directory or the path must be fully specified.
      - e.g.  For ```root/Users/username``` the **username** directory can be accessed from **Users**.
      - To change to a directory not contained within **Users**, we must specify the full path ```root/Users/```
    - ```cd ..``` changes the directory one level up.
      - e.g.  Using ```cd ..``` on the path ```root/Users/username``` changes the directory to ```root/Users```
      - ```cd ..``` can also be combined with a path from the directory up to go back a directory and proceed to the specified path.
      - e.g.  ```cd ../RDCLder/Documents``` will take you from **username** to **Users** and then to the specified path.
  - **mkdir**:  "Make Directory".  Takes a directory name as an argument and creates it in the working directory.
  - **touch**:  Takes a file name as an argument creates that file in the working directory.

- Copy and Pasting
  - **cp**:  Copies specified file(s).
  - Syntax:  ```cp file``` or ```cp directory/file newdirectory/```
    - The first command copies the specified file(s).
    - The second command copies the specified file(s) to a specified location relative to the working directory.
  - Options:
    - ```*``` selects all files in the working directory.
      - ```*``` can be preceded with a character to specify all files starting with that character.
      - ```*``` can be proceeded with a file type to specify all files of that type.
  - Examples
    - ```m*.txt``` specifies all files starting with a m and ending with .txt.

- Moving
  - **mv**:  Moves specified file(s).
  - Syntax:  ```mv file newdirectory/```

---

# Windows PowerShell
