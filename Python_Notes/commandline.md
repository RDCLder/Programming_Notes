# The Command Line

## Navigation and Creation

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

---

## Manipulation

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
  - **mv**:  Moves specified file/directory.
  - Syntax:  ```mv file newdirectory/```

- Removing
  - **rm**:  Removes specified file/directory.
  - Syntax:  ```rm file```
  - Options:
    - ```-r``` stands for "recursive" and is used to delete a directory and all its contents.
  - There is no "un-delete" command so all removals are permanent.

---

## Redirection

- General
  - Definition:  Redirection is the act of directing I/O of a command between different files and programs and chaining them together in a pipeline.
  - Syntax:  ```input [symbol] output location```
    - ```>``` redirects output of a preceding command to a proceeding file, overwriting previous content.
    - ```>>``` redirects output of a preceding command to a proceeding file, appending to previous content.
    - ```<``` redirects proceeding input to a preceding command.
    - ```|``` redirects standard output of a preceding command as the input to the proceeding command.
    
  - I/O Definitions
    - Standard Input:  ```stdin``` information input into the terminal through the keyboard or input device.
    - Standard Output:  ```stdout``` information output after a process is executed.
    - Standard Error:  ```stderr``` error message output after a process fails.
  
- Commands
  - **echo**:  Accepts a standard input and returns it to the terminal as a standard output.
    - Syntax:  ```echo 'string'```
    - e.g. ```echo "Hello world!"```
  - **cat**:  Outputs content of a file to the terminal.
    - Syntax:  ```cat file > location```
      - Default location is terminal if not specified.
    - e.g. ```cat oceans.txt > continents.txt```
      - This would replace the content of continents.txt with that of oceans.txt.
  - **wc**:  "Word Count".  Counts the words in a file.
  - **sort**:  Takes a input and returns it sorted alphabetically as the output.
  - **uniq**:  Takes a input and returns the number of unique, adjacent instances as the output.
    - If repeated instances are not directly adjacent, they will remain.  Sort command is commonly used to address this.
  - **grep**:  "Global Regular Expression Point".  Searches files for lines that match an input pattern and returns them.
    - Syntax:  ```grep 'string' file/location```
    - Case sensitive.  ```-i``` renders the command case insensitive.
    - ```-R``` limits the search to a specified directory.
    - ```-l``` limits the search to only files.
  - **sed**:  "Stream Editor".  Accepts an input and modifies it based on an expression before returning an output.
    - Syntax:  ```sed 'front_expression/search_string/replacement_string/back_expression' location```
      - The expression denotes what to do.  See expressions.
      - The search_string is the string being searched and replaced with the replacement_string.
    - Expressions
      - ```s``` front expression.  Substitutes all instances of a specified string with a replacement string.
      - ```g``` back expression.  Designates a global search.
    - e.g.  ```sed 's/snow/rain/g'
      - This searches for all instances of ```snow``` and replaces them with ```rain```
