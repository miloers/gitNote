#### Note from liaoxuefeng
##### order1
初始化一个Git仓库，使用git init命令。

添加文件到Git仓库，分两步：

第一步，使用命令git add <file>，注意，可反复多次使用，添加多个文件；

第二步，使用命令git commit，完成。

##### order2

要随时掌握工作区的状态，使用git status命令。

如果git status告诉你有文件被修改过，用git diff可以查看修改内容。

##### order3

HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令git reset --hard commit_id。

穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本。

git log --pretty=oneline

要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本。

##### order4

每次修改，如果不add到暂存区，那就不会加入到commit中。

##### order5

当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。

当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD file，就回到了场景1，第二步按场景1操作

##### order6

命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

在rm file.txt后 仓库还是有文件的
彻底删除 git rm file.txt ->git commit -m"remove file.txt"


##### order7

添加远程库
本机里创建SSH KEY
本机生成 id_rsa 和 id_rsa.pub
创建远成仓库后新建ssh_key与id_rsa.pub相匹配。（本地创建的id_ras.pub复制到远程仓库新建的ssh_key里）

##### order8

