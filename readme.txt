1,安装完成后，还需最后一步这是，在命令中输入
git config –global user.name  “username”
git config –global user.email   “email”
2,打开需要管理的文件夹
git init  
就可以把这个目录变成git可以管理的仓库了，目录下生成  .git目录
3，把一个文件放在git仓库里面
git add readme.txt
git commit –m “worte a readme file”
4,查看历史日志
git log
5,返回上一个版本
git reset --hard HEAD^
6，回到指定的版本
git reset --hard 1094a
7，用来记录你的每一次命令
git reglog 

这样你就可以穿梭其中的任意的版本了

8,提交后，用以下命令可以查看工作区和版本库里面最新版本的区别
git diff HEAD -- readme.txt

9，文件必须放在暂存区 才能提交到版本库里面

10，你可以发现，Git会告诉你，git checkout -- file可以丢弃工作区的修改：
git checkout -- readme.txt

11，如果你不想提交的文件在缓存区，可以撤销到工作区
git reset HEAD readme.txt
然后在丢弃工作区的修改
git checkout -- readme.txt

12,删除文件
rm a.txt

13,git status 可以查看你做了什么操作




