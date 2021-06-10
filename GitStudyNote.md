# Git使用手册



## 1 . 工作区、暂存区、版本库、远程版本库

#### 第一步： 使用 'git add' 命令将文件从工作区（即硬盘）存入暂存区中

#### 第二步： 使用 'git commit' 命令将暂存区的文件夹存入版本库中



## 2. 版本回退

#### 	1.修改文件后，即使不关闭文件，使用 'git status' 命令，也能发现文件被修改——"Changes not staged for commit."

#### 	2.修改文件后，先用 'git add' 命令将文件存入暂存区中；此时再使用'git status' 命令可查看**仓库**当前状态，会显示可被提交的修改——"Changes to be commited."

## 3. 将本地项目上传到GitHub

#### 1.创建GitHub仓库。选择"Add a README File"会自动生成一个叫"main"的分支。可设置默认生成的分支命名为"master"，这样便与本地版本库相同。

#### 2.远程库输入错误时，可用'git remote -v'查看添加的远程库，再用'git remote remove origin'删除。



## 4.GitBash上传本地项目到GitHub

#### 1.关联远程库：

#### git remote add origin git@github.com:xxxxx/xxxxx.git

#### 2.提交所有内容至远程库：

#### git push -u origin master

#### -u 参数会把本地分支master和远程分支关联起来

#### 3.创建并切换分支

####  创建分支：git branch xxx 

#### 切换分支：git switch xxx

#### 提交后，再使用 git push origin xxx ,就会把xxx分支提交到远程库中

#### 在GitHub上，可以合并现有分支。

#### commit新分支时，如果不使用-m参数输入提交信息，会出现：

> E325: ATTENTION
>
> Found a swap file by the name "..."

#### 输入Q退出后，会提示：

> Waiting for your editor to close the file... erro: There was a problem with the editor 'vi'.
>
> Please supply the message using either -m or -F opition 

#### 出现原因及解决方案可参考：

https://stackoverflow.com/questions/13361729/found-a-swap-file-by-the-name

https://blog.csdn.net/qq_32452623/article/details/78395832?utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-2.control&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EBlogCommendFromMachineLearnPai2%7Edefault-2.control

#### 4.当远程库存在本地库没有的文件时：

> error: failed to push some refs to 'github.com:xxxx/xxxx.git'
>
> 提示：由于远程库存在本地所没有的文件，更新被拒绝。这通常是因为其他库正向该远程库推送。在再次推送之前，你可能想要先合并（'git pull ...'）远程的改变

#### 先使用"git fetch origin xxx"获取远程分支

#### 此时会得到一个"FETCH_HEAD"，包含某个分支在远程库上的最新状态。

#### 再使用"git merge FETCH_HEAD"，将拉取下来的最新内容合并到当前分支中







