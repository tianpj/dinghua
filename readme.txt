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