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
