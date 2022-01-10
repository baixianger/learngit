# Learning Git

Git is a version control system
Git is free software.

## 新建一个git repository

### 新建一个目录
```
$ mkdir learngit
$ cd learngit
$ pwd
```
### 在改目录下输入如下命令
```
$ git init
Initialized empty Git repository in /<your path>/learngit/.git

## 增加README.txt文件

### 用文字工具新建一个README.txt编辑后保存
```
$ vi README.txt
```
### 输入git add <filedir>命令
```
$ git add README.txt
```
### 输入git commit -m <message>命令
```
$ git commit -m 'the commit you want add'

## 版本回退
1. HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。

2. 穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。

3. 要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

## 工作区和暂存区

1. 第一步是用git add把文件添加进去，实际上就是把文件修改添加到暂存区；

2. 第二步是用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。

## 管理修改

为什么Git比其他版本控制系统设计得优秀，因为Git跟踪并管理的是修改，而非文件。
```
git status
```
## 测销修改

- 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令
`git checkout -- <file>` 或者 `git restore <file>`

- 场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令`git reset HEAD <file>` 或者 `git restore --staged <file>`，就回到了场景1，第二步按场景1操作。

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
