Git is a version control system.
Git is free software.

git init
git add
git commit -m "XXX"
git status
git diff

版本回退
git log  // 提交历史 - 回退到某个历史版本
git reset --hard HEAD^  / HEAD^^ / HEAD~100 / 62a1c (commit id前几位)  ； 把暂存区的修改回退到工作区
git reflog // 历史命令 - 回到未来的某个版本

工作区
Working Directory

版本库 .git
Repository
git add 将文件修改添加到 暂缓区（stage）
git commit 将暂缓区的所有内容提交到当前分支

丢弃工作区的修改
git checkout -- file

丢弃暂存区的修改
git reset HEAD <file> + git checkout -- file

丢弃版本库的修改
版本回退

删除文件
git rm + git commit

git checkout
其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

远程仓库
本地Git仓库和GitHub仓库之间的传输是通过SSH加密
创建SSH Key：
$ ssh-keygen -t rsa -C "youremail@example.com"
在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件
登陆GitHub，打开“Account settings”，“SSH Keys”页面
点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容
