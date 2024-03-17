

# 本地文件夹推送到远程新建的空项目

git init



git add .  

//添加到暂存区



git commit -m "第一次创建项目"

//提交



```
git remote add origin https://github.com/WGJ18334581632/www.git
```

//和远程项目进行关联



git push -u origin dev:release/caigou_v1.0 

//推送【注意：写的远程分支为release/caigou_v1.0 ，不包含remotes/origion】



# git切换到指定远程分支

git branch -a 

//查看所有分支

![1708561186346](C:\Users\WGJ\AppData\Roaming\Typora\typora-user-images\1708561186346.png)

当前分支前带*，红色为远程分支【注意加有：remote/origion】



git checkout -b dev origin/release/caigou_v1.0

//新建了本地分支dev；

//本地dev分支和 远程的release/caigou_v1.0分支关联了起来



$ git branch -vv

//**查看本地分支及追踪的分支**



# 多人合作开发，合并远程冲突

**拉取远程分支的最新代码：**

git pull origin main //默认为origin【 `origin` 是你远程仓库的别名。 】 【和git remote add origin中的origin相对应】



**补充：git pull和git fetch的区别？**：

- 从远程仓库下载最新的提交对象，并尝试自动合并（merge）这些更改到你当前的工作分支。
- 它实际上是 `git fetch` 和 `git merge` 两个命令的组合。



解决冲突之前先把本地代码 提交到本地git中

git add .

git commit -m "www更www新"



**解决冲突：**

![1710666438393](C:\Users\WGJ\AppData\Roaming\Typora\typora-user-images\1710666438393.png)



然后推送