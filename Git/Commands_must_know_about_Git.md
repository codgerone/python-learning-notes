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

