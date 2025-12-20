# Commands must know about Git

## 1. `git init`
Creat a new repository. Only once for each repository.

## 2. `git status`
To see which files have been modified, and whether they have been committed.

> **Note:** *Always recommend to check **git status** before using the command `git add` or `git commit`*.

## 3. `git add`

This command can upload changes to the ***Staging Area***, here are three ways to use it:

- **`git add <file name>`** : 

   only add the specified file.


- **`git add <folder name>/`**: 

  add the whole folder.
- **`git add .`** :
  
  add the whole directory.

## 4. `git commit`
Commit the changes in the Staging Area to git:

**`git commit -m "message"`**

## 5. `git restore`
This command can revert the files to a previous state, two ways to use it:

- **`git restore <file name>`**:

  undo modifications in the **working directory**, revert the file's content to match the state of the last commit(HEAD).

> *Note: Olny works on **tracked files**.*

- **`git restore --staged <file name>`**:

  remove files from **staging area**, revert the files back from "staged" to "unstaged".


**💡 Pro Tips:**

- To restore **all** modified files in the current directory:  
  **`git restore .`**
- To unstage **everything**:  
  **`git restore --staged .`**

