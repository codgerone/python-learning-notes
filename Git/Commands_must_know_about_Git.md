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

## 4. `git restore`
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

## 5. `git commit`
Commit the changes in the Staging Area to git:

**`git commit -m "message"`**

## 6. `git remote`

- **`git remote add <remote_name> <remote_repo_URL>`**
- **`git remote remove <remote_name>`**
- **`git remote rename <old_name> <new_name>`**
- **`git remote set-url <remote_name> <new_URL>`**
- **`git remote -v`**

## 7. `git branch`

- 查看分支
`git branch`
带*标记的为当前所在分支

- 创建分支
`git branch xxx`

- 切换分支
`git switch xxx`

- 创建并切换
`git switch -c xxx`

- 查看所有分支
`git branch -a`

- 推送分支
`git push -u origin xxx`

- 合并分支
`git merge xxx`

- 删除分支
`git branch -d xxx`

- **`git branch`**:

  check the local branch

- **`git branch -vv`**:

  check the current upstream (the default remote branch connecting to the local branch)

- **`git branch -u <remote_name>/<remote_branch>`**:

  set the upstream to <remote_name>/<remote_branch>

## 8. `git push`
- **`git push`**:

  *euqal to `git push <upstream_remote> <local_branch>`*
- **`git push <remote> <local_branch>`**:

  *for example: `git push Learning_notes main`*

- **`git push -u <remote> <local_branch>`**:

  *set the upstream and push at the same time, for example:*

  *`git push -u python_learning_notes main`*

## 9. `git pull`

- **`git pull`**:

   *equal to `git pull <upstream_remote> <local_branch>`* 

- **`git pull <remote> <local_branch>`**

## 10. `git fetch`
