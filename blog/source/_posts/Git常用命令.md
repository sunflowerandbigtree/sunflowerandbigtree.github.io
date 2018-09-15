---
title: Git常用命令
date: 2018-09-14 23:17:21
tags:
---
- Git安装
```r
$ git
The program 'git' is currently not installed. You can install it by typing:
sudo apt-get install git
```


- Git设置
```r
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```


- 初始化
```r
$ git init

$ git add <file>

$ git commit -m <message>
```


- 查看Git状态
```r
$ git status

$ git diff
```


- 查看历史版本
```r
$ git log

$ git reflog
```


- 撤销修改
```r
$ git checkout -- file

$ git reset HEAD <file>
```


- 删除文件
```r
$ git rm
```


- 添加远程仓库
```r
$ git remote add origin git@server-name:path/repo-name.git

$ git push -u origin master

$ git push origin master
```


- 从远程仓库克隆
```r
$ git clone
```


- 分支管理
```r
查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>
```


- 从远程仓库拉取分支
```r
$ git pull
```