## 学习python的第33天

Linux下安装软件的几种方式
1.包管理工具
yum  
	install 安装
	remove 删除
	search  查找
	list installed  列出已安装的
	info  查看信息
rpm 
	-ivh <rpm-file-name>  安装
	-e 移除
	-qa 查找

命令 | xargs 命令  把前一个命令的输出作为后一个命令的参数

2.二进制的安装程序

3.下载  解压  免安装  通常需要配置环境变量才能使用

4.源代码构建安装

	make && make install



### 如何使用Git

git init 初始一个空的仓库

git add 文件名   将文件纳入版本控制，文件放入暂存区，并没有真正版本控制

git status  查看文件的状态

git commit -m 原因   提交（必须写原因）

git log 查看日志

git reset --hard 版本号（前6位就可以） 回到版本号的版本

git reflog  查看之前的所有操作版本

git clone url 地址  把项目从云端克隆到本地

git push  origin master从本地推送到服务器

git pull  地址    从远端服务器更新代码

git rm --cached <filename> 从暂存区删除文件
	
git checkout -- <filename>  把暂存区里的拿回来覆盖掉工作区文件
	
git remote add origin 地址  把远端仓库和本地仓库关联起来


#####window下查看文件的命令是dir
	cls 清屏
	-a 显示隐藏文件

####如何将本地的文件推送到远端仓库
第一次
1.创建一个文件夹

2.git init 初始化本地仓库

3.git remote add origin 远端网址   将远端仓库和本地仓库建立连接

4.git clone 远端网址 master  将远端仓库的文件同步到本地

5.git add 文件名  将文件从工作区存到暂存区

6.git status  查看暂存区文件

7.git commit -m '提交信息'  将暂存区的内容提交给本地仓库

8.git push -u origin master 将本地已经实施了版本控制的内容push到远端仓库
                            分支名 将分支推到远端
以后push的时候就不需要 -u 了

9.git pull  从远端更新本地仓库

git branch 查看分支

git branch <name>  新建分支
	
git checkout <分支的name>  切换分支

		  -b <分支的名字>  建立分支并且切换到该分支
		  
如果要在master上合并分支需要先切回到master分支

git merge <name>  合并分支

删除分支：
git branch -d <name>  如果分支还没有合并要删除可以使用
	
git branch -D <name>  强行删除分支

git reset HEAD <filename> 从暂存区移除文件
	
git log 查看日志

git reflog  查看日志(可以查看到以前的版本)

git reset HEAD^  回到上一个版本

git reset <id>  回到id指定的历史版本
	
git reset --hard <id>  回到ID指定的历史版本并让工作区和指定版本保持一致

git push origin <branchname> 将本地内容推到git上
	
git push --force 强行推送
