## learn-git-dqq
# 学习git

创建文件，切换分支，分支合并，提交
Git 与 github

新建项目文件 在github中新建仓库

登录github
点击 + New repository
设置项目名和项目描述等信息，点击create repository
在命令行中进入本地指定的文件夹（存放位置）


或   使用命令行新建项目文件

> mkdir xxxx     // 创建文件夹
> cd xxxxx       // cd 表示进入某个文件夹
> cd..           // 表示返回上一级
> git clone git@github.com:blues007/learn-git-dqq.git        // 克隆github的项目

设置一下你的用户名与邮箱，与github上的保持一致即可  【第一次配置时 设置一次即可】
> git config --global user.name "blues007"
> git config --global user.email "dq1530370173@163.com"

> git config --global user.name             //查看用户名
> git config --global user.email           //查看邮箱

项目克隆到本地，默认会在master分支上,新建分支先开发好功能，上线的时候合并到master分支上
> git branch            // 查看当前分支
> git branch new1       // 创建分支
> git checkout new1     // 切换到分支
    > git branch new2             // 创建新分支,并切换到该新分支
    > git branch checkout new2    // 切换到该分支2
    > git merge new1      // 将new1分支的内容，往master分支上合并 要先切换到mastera主分支上(分支new1合并到master)
	> git branch  -d   new1          // 删除已经合并过的分支
	> git branch  --merged           // 查看与当前分支合并过的分支
	> git branch  --no-merged        // 查看没有与当前分支合并过的分支
	> git branch -D new2             // 强制删除没有合并过的分支
//合并分支，或者分支推送，继续走下面 删除分支，合并分支，都
> git status                   // 随意进行一些修改，查看哪些文件被修改
> git add .                    // 添加修改到暂存区，表示提交所有文件
> git commit -m "注释"          // 从暂存区提交到本地仓库
	> git diff                     // 工作区与暂存区的对比
	> git push origin new1         // 从本地仓库推送到远程服务器，这个过程会在远程仓库新建上面new1分支
> git pull                     // 每次推送前，需要从远程拉取一次代码 自动合并（多人开发，代码同步）
> git push origin master       // 往远程仓库提交


----无分支----
git add .
git commit -m "注释"u//pdate"
git pull
git push origin master

