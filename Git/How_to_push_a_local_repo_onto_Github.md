# 如何把一个本地仓库上传到Github

### 整体思路：

1. 在GitHub建立一个远程仓库
2. 在本地建立与远程仓库的连接
3. 推送代码到远程仓库

## 1. 在GitHub建立远程仓库

### （0） 安装 GitHub 官方命令行工具 GitHub CLI (gh) 
- 在终端运行：

```bash
windget install GitHub.cli
```
> *winget 是微软自带的 “操作系统级” 包管理工具，对比 pip 为 “语言级” 包管理工具。此命令用于直接在 windows 操作系统中安装 GitHub CLI。（直接装在操作系统里，不受限于VS Code或任何虚拟环境，操作系统级的安装）。*

> *这辈子，在这台电脑上，安装过这一次，就够了。*

- 安装完后把电脑绑定Github账号：
```bash
gh auth login
```

### （1） 建立Github远程仓库
利用 Github CLI 工具，可以直接在本地远程指挥 Github 创建仓库，而不用到 Github 的网页上进行创建：
```bash
gh repo create <repo name> --public
```

## 2. 建立本地与远程仓库的连接
- ### 在终端输入Git的远程仓库管理命令：
```bash
git remote add <远程仓库别名> <远程仓库URL>
```
示例：
```bash
git remote add Python_learning_notes https://github.com/codgerone/Python_learning_notes.git
```
```bash
git remote add Learning_notes https://github.com/codgerone/Learning_notes.git
```

> 💡**强烈建议：** *在 Git 中每个远程仓库的别名，就根要建立连接的远程仓库名称起成一样就行，这样不会错乱。不要起名 orgin (origin是默认的远端仓库别名) 。*

- ### 建立联系后可用的“检查”命令：
```bash
git remote -v
```
> *`-v` 是 verbose (详细)的缩写。该命令会显示在当前这个根目录（root direcotry / working directory）中创建过的所有远程连接。*

- ### 移除已创建的远程连接：
```bash
git remote remove <别名>
```
- ### 修改已建立的远程连接的别名：
```bash
git remote rename <旧别名> <新别名>
```
- ### 修改已建立的远程连接的URL:
```bash
git remote set-url <别名> <新的URL>
```
### 小结：
| 目标 | 命令 |
| :--- | :--- |
| **查看**当前所有远程连接 | `git remote -v` |
| **创建**新的远程连接 | `git remote add <name> <url>` |
| **删除**某个连接 | `git remote remove <name>` |
| **改名**（别名） | `git remote rename <old> <new>` |
| **改地址** (URL) | `git remote set-url <name> <new_url>` |


## 3. 把代码推到远程仓库

```bash
git push <远程仓库别名> <要传送的本地分支名>
```
示例：
```bash
git push python_learning_notes main
```

## 4. `git push`的本质

💡 `git push`的 **本质** 是把远端分支指针，从它现在的位置，推进到本地分支指针的位置；如果中间缺了对象，就补齐。

即对照以下两个对象（***comparison***），并补齐差集，对照的两个对象为：
```md
本地分支的最新提交（HEAD / 分支指针）
refs/heads/main
vs
远端对应分支的最新提交（远端分支跟踪指针）
refs/remotes/origin/main
```

最终，该命令会把本地分支上 “尚未推送到远程仓库的所有提交（commits）” 一次性推送推送上去，而不是只推送本次commit的内容。

> **注意：** 远端分支跟踪指针不是远端仓库里的指针本体，而只是本地保存的“远端状态快照”，可由`git fetch`把本地的远端分支跟踪指针更新到与远端仓库的本体指针一致的位置。

## 