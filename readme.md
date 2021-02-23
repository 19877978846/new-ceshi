# readme文档
- 项目说明文档
- 一般与项目放一起

# git操作

## 初始化版本库
- 初始化成功后，当前目录后面有个(master)
- 初始化成功后，有个.git文件(不要管他)

## 工作区
- 持有实际文件
- 我们平时增删改的文件都是工作区的内容

## 暂存区
- 可以理解为我们看不到的地方
- 本地仓库的一个主要组成部分

## 本地仓库
- 可以理解为我们看不到的地方
- 也是存在于用户电脑中的
- 用于存储项目代码以及项目记录等信息

## 提交到暂存区
- git add 文件名
- 将工作区的变动提交到暂存区

## 查看工作区和暂存区的状态
- git status 
- 查看工作区和暂存区的状态

## 提交到本地仓库
- git commit -m '提交注释'
- 将代码从暂存区提交到本地仓库
- git status 查看提示状态：工作区是干净的，没有任何东西需要提交

## 本地操作关键步骤
1、 git init（第一次需要）
2、 git add .
3、 git commit -m '注释'

## 查看状态
- git status
- 查看工作区和暂存区的状态(增删改)

## 查看日志
- git log 查看完整日志
- git reflog 查看简单日志

## 版本回退 
- 注意先把当前代码提交到本地仓库
- git reset --hard HEAD^ 回退到上一个版本
- git reset --hard 版本号(git log 获取版本号)

- 工作区的代码自动变成恢复的指定版本

## 查看变动
- git diff 文件名
- 会列出该文件前后的差异

## 创建远程仓库
- 进入github官网
- 创建一个新的远程仓库

## 将本地仓库与远程仓库关联
- git remote add origin 你的远程仓库地址
- git remote -v 查看本地仓库关联的远程仓库地址

## 将本地仓库提交到远程仓库
- git push -u origin master 第一次提交到远程
- git push 将本地仓库提交到远程仓库
- -u origin master 设置默认的提交地址和分支 

## 正常提交(非第一次提交)***(重点)
- git add . (提交到暂存区)
- git commit -m '注释' (提交到本地仓库)
- git pull 先更新远程到本地
- git push (提交到远程仓库，(默认提交到origin上的master分支))

## 修改关联的远程仓库地址
- git remote rm origin (删除原来的地址)
- git remote add origin 你的ssh地址 (修改关联的地址)

## 更新代码
- 确保自己的工作区的代码先提交到本地仓库
- 然后再从远程更新到本地 git pull
- git clone 远程仓库地址 (克隆到本地)

## 其他人修改
。。。。

## 其他人再次修改
。。。。。

## 分支操作
- git branch (查看当前分支)
- 当前分支名前有个*
- git branch 分支名 (创建分支)
- git checkout 分支名 (切换分支)
- git merge 分支名 (合并某分支到当前分支)
- git branch -d 分支名 (删除某分支)
- git push origin 分支名 (提交某分支到远程)
- git pull origin 分支名 (将远程某个分支更新到本地仓库)

## fetch和pull的区别
1、 他们都用于从远程更新到本地
2、 git fetch不会自动合并到当前分支(不会merge)
3、 git pull会自动合并到当前分支(会merge)

## 忽略列表
- 在项目中创建文件 .gitignore 
- 把不需要提交到远程仓库的文件或目录写在忽略列表中

## test分支
  
- 添加内容。。。123456
- 添加内容。。。
