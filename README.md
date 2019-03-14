# gitguide
git guide
# 1、配置
git config --global user.name "michael"
git config --global user.email "michael@xxx.com"
global对所有repository生效，也可以不加针对不同的repository生效。

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
