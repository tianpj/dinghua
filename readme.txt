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
使用  git status 知道你删除了a.txt 
如果你确定删除a.txt
git rm a.txt
git commit -m "remove a.txt"
这两行命令

另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
git checkout -- test.txt
（只适用还没有做上面两行命令）


13,git status 可以查看你做了什么操作

14，管理库 GitHub
	ssh-keygen -t rsa -C "youremail@example.com"
	登陆GitHub，打开“Account settings”，“SSH Keys”页面：
	点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容：
	点“Add Key”，你就应该看到已经添加的Key：
	
15，上传文件到github
git remote add origin https://github.com/tianpj/dinghua.git
git push -u origin master

16，现在本地提交就可以使用
git push origin master

17，要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；

分布式版本系统的最大好处之一是在本地工作完全不需要考虑远程库的存在，也就是有没有联网都可以正常工作，
而SVN在没有联网的时候是拒绝干活的！当有网络的时候，再把本地提交推送一下就完成了同步，真是太方便了！

18，下载一个远程库
git clone git@github.com:michaelliao/gitskills.git

19，分支管理
	查看分支：git branch

	创建分支：git branch <name>

	切换分支：git checkout <name>

	创建+切换分支：git checkout -b <name>

	合并某分支到当前分支：git merge <name>

	删除分支：git branch -d <name>
	
20,当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。

解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交。

用git log --graph命令可以看到分支合并图。

21,分支管理策略
Git分支十分强大，在团队开发中应该充分应用。
合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，
而fast forward合并就看不出来曾经做过合并。
 git merge --no-ff -m "merge with no-ff" dev
 git log（查看历史合并分支）