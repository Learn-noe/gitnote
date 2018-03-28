## 1、查看远程分支：
	$ git branch -a 
	   * br-2.1.2.2  
		master  
 		 remotes/origin/HEAD -> origin/master  
 		 remotes/origin/br-2.1.2.1  
  		 remotes/origin/br-2.1.2.2  
  		 remotes/origin/br-2.1.3  
		 remotes/origin/master  
## 2、查看本地分支：
	$ git branch  
		* br-2.1.2.2  
  		master  
## 3、创建分支：
	$ git branch test


	$ git branch
		* br-2.1.2.2
  			master
  			test
	 把分支推送到远程分支
		$ git push origin test
## 4、切换到分支test

	$ git branch
		* br-2.1.2.2
  		master
  		test

		M 表示cong 原来分支（上一次修改没有提交br-2.1.2.2）带过来的修改
		$ git checkout test
		M       jingwei-server/src/main/java/com/taobao/jingwei/server/service/cmd/GetCustomerTarCmd.java
		M       jingwei-server/src/main/java/com/taobao/jingwei/server/util/ServerUtil.java
		Switched to branch 'test'

	$ git branch
  		br-2.1.2.2
  		master
		* test
## 5、删除本地分支
    $ git checkout br-2.1.2.2
        M       jingwei-server/src/main/java/com/taobao/jingwei/server/service/cmd/GetCustomerTarCmd.java
        M       jingwei-server/src/main/java/com/taobao/jingwei/server/util/ServerUtil.java
        Switched to branch 'br-2.1.2.2'

       shuohailhl@SHUOHAILHL-PC /f/ggg/jingwei (br-2.1.2.2)
    $ git br
      * br-2.1.2.2
        master
        test

      shuohailhl@SHUOHAILHL-PC /f/ggg/jingwei (br-2.1.2.2)
    $ git br -d test
       Deleted branch test (was 17d28d9).

       shuohailhl@SHUOHAILHL-PC /f/ggg/jingwei (br-2.1.2.2)
    $ git br
       * br-2.1.2.2
        master
## 6、查看本地和远程分支  -a。前面带*号的代表你当前工作目录所处的分支
    remotes/origin/HEAD -> origin/master #啥意思呢？  
	$ git remote  -v  
		origin  git@xxxx/jingwei.git (fetch)  
		origin  git@xxxx/jingwei.git (push) 

	shuohailhl@SHUOHAILHL-PC /f/ggg/jingwei (test)  
    $ git branch -a  
      br-2.1.2.2  
      master  
    * test  
      remotes/origin/HEAD -> origin/master  
      remotes/origin/br-2.1.2.1  
      remotes/origin/br-2.1.2.2  
      remotes/origin/br-2.1.3  
      remotes/origin/master   

## 7、删除远程版本
	git push origin :br-1.0.0  
## 删除远程分支  
### git branch -r -d origin/branch-name  
### git push origin :branch-name 