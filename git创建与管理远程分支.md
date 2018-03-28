## 1、远程分支就是本地分支push到服务器上的时候产生的。比如master就是一个典型的远程分支（默认）。
	$ git push origin master
## 2、除了master之外我们还可以随便创建分支，然后push到服务器上去 例如：
	$ git push origin develop 
## 3、远程分支和本地分支需要区分，所以，再从服务器上拉取特定分支的时候需要制定特定分支的名字
	$ git checkout --track origin/develop 
 /* 注意该命令带有--track参数，所以要求git1.6.4以上  这样git就会自动切换到develop分支 */
## 4、同步本地远程分支
	$git fetch origin
## 5、提交分支数据到远程服务器
	$ git push origin <local_branch_name>:<remote_branch_name>
	例如：
		$ git push origin develop:develop
	如果在当前develop分之下，也可以直接
		$ git push
## 6、删除远程分支develop
	$ got push origin :develop
##  第一次创建的时候服务器上面没有任何分支（使用git init --bare）.那么在本地创建了之后需要推送一个分支到服务器上面。
## 即：第一次push必须这样写 git push origin master:master
    git checkout master         //取出master版本的head。
    git checkout tag_name    //在当前分支上 取出 tag_name 的版本
    git checkout  master file_name  //放弃当前对文件file_name的修改
## git checkout branch_name tag_name //取指定分支branch_name的tag_name的版本
## git checkout  commit_id  file_name  //取文件file_name的 在commit_id是的版本。
## commit_id为 git commit 时的sha值。
## 列出某一个commit ID(XXXXXXXXXXXXXXXX) 对应的补丁：
   $ git log -1 -p XXXXXXXXXXXXXXXX
   $ git format-patch -1 XXXXXXXXXXXXXXXX <===-1不可省略
        --stdout         //打印到标准输出
   $ git show XXXXXXXXXXXXXXXX
   $ git diff-tree -p XXXXXXXXXXXXXXXX