# Git使用手册



## 1 . 工作区、暂存区、版本库、远程版本库

#### 第一步： 使用 'git add' 命令将文件从工作区（即硬盘）存入暂存区中

#### 第二步： 使用 'git commit' 命令将暂存区的文件夹存入版本库中

## 2. 版本回退

#### 	1.修改文件后，即使不关闭文件，使用 'git status' 命令，也能发现文件被修改——"Changes not staged for commit."

#### 	2.修改文件后，先用 'git add' 命令将文件存入暂存区中；此时再使用'git status' 命令可查看**仓库**当前状态，会显示可被提交的修改——"Changes to be commited."

## 3. 将本地项目上传到GitHub

#### 1.创建GitHub仓库。选择"Add a README File"会默认添加一个叫"main"的分支。可在设置中默认生成的分支命名为"master"，这样便与本地版本库相同。



