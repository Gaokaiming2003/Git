# git

## 常用命令

### 初始化仓库

git init

### 克隆仓库

git clone <repository_url>

### 添加文件到暂存区

git add \<file>

### 提交更改

git commit -m "Commit message"

### 查看状态

git status

### 查看提交历史

git log

### 创建分支

git branch <branch_name>

### 切换分支

git checkout <branch_name>

git switch <branch_name>

### 创建并切换到新分支

git checkout -b <branch_name>
git switch -c <branch_name>

### 合并分支

git merge <branch_name>

### 拉取远程分支的更改

git pull origin <branch_name>

### 推送本地分支到远程仓库

git push origin <branch_name>

## 查看远程仓库信息

git remote -v

### 解决冲突（手动解决后再提交）

### 查看分支列表

git branch

### 查看远程分支列表

git branch -r

### 查看所有分支（本地和远程）

git branch -a

### 创建标签

git tag <tag_name>

### 推送标签到远程仓库

git push origin --tags

## 一个完整的步骤

```null
git init    //在项目文件夹路径下
git remote add <remote_alias> <remote_repository_url>
git add .
git commit -m "Initial commit"
git push -u <remote_alias> master

```

## 建立新的分支

```null
git branch        查看当前分支
git branch <branch_name>  创建新的分支， <branch_name>是分支名称
git checkout <branch_name>  切换到<branch_name>分支
(git switch <branch_name>      git version 2.23及以上)
git checkout -b <branch_name> 合并当前分支和<branch_name>分支并切换到<branch_name>分支
git switch -c <branch_name>
```

## 将本地仓库的修改推送到远程仓库

`git push <remote_alias> <branch>`

* <remote_alias>:远程仓库的名称。通常情况下为origin,这是默认的远程仓库的名称。
* \<branch>:要推送的分支的名称。

如果已经设置了默认远程仓库，可以省略：`git push`

### 选项和用法

#### `-u`或`--set-upstream`:将本地分支与远程分支关联,以后可以简化推送命令

`git push -u orgin master`

#### `--force`:强制推送，覆盖远程仓库上的内容。

`git push --force origin master`

#### `--all`:推送所有分支到远程仓库

`git push --all origin`

#### `-tags`:推送所有标签到远程仓库

`git push --tags origin`