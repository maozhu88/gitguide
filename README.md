# gitguide
git guide常用配置
# 1、配置
git config --global user.name "michael"
git config --global user.email "michael@xxx.com"
global对所有repository生效，也可以不加针对不同的repository生效。
--local配置当前仓库

#2、仓库
两种创建仓库的方式
1、创建一个空的仓库
2、拷贝一个已有仓库

#3、修改操作
1、git add 添加修改
2、git commit -m "note" 提交修改

#4、查看修改
1、查看修改记录
git log --pretty=oneline
2、回退修改
HEAD表示当前版本，HEAD^表示前一个版本，HEAD~N表示前N个版本。
git reset --hard HEAD^返回上一个版本，或者
git reset --hard 409aa(hash ID的前几位)
3、返回回退之前的版本
git reflog会记录每次修改。
git reset --hard  id（回退前版本ID即可）



#本地仓库
#1、初始化
git init

#2、添加修改
git add file
git add . 提交全部修改到暂存区 

#3、提交
git commit -m "comment"

#4、查看状态
git status

#5、查看修改内容
git diff file
git diff HEAD^ HEAD，比较上次递交和上上次之前的区别。

#6、查看日志
git log

#7、回到之前版本
git reset versionno(git log查看)
git reset三种模式，
--soft仅影响HEAD
--mixed（默认）影响HEAD和暂存区
--hard影响HEAD，暂存区，文件内容

#8、回到commit或add时的版本
git checkout

#9、删除文件
git rm file
git commit -m "rm file"



#远程仓库
#1、本地生成sshkey
ssh-keygen -t rsa -C "youremail@example.com"
一路回车，生成.ssh文件夹，id_rsa为私钥，id_rsa.pub为公钥

#2、远程添加公钥
打开GitHub，SSH and GPG keys中添加SSH keys添加上述id_rsa.pub内容。

#3、测试远程连接
ssh -T git@github.com
ssh -T -p 443 git@ssh.github.com
不加-p默认为22端口，注意windows防火墙需要允许22端口的in操作。

#4、获取远程仓库pull
git pull git@github.com:maozhu88/gitguide.git


