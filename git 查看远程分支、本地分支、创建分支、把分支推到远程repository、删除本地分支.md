## 1���鿴Զ�̷�֧��
	$ git branch -a 
	   * br-2.1.2.2  
		master  
 		 remotes/origin/HEAD -> origin/master  
 		 remotes/origin/br-2.1.2.1  
  		 remotes/origin/br-2.1.2.2  
  		 remotes/origin/br-2.1.3  
		 remotes/origin/master  
## 2���鿴���ط�֧��
	$ git branch  
		* br-2.1.2.2  
  		master  
## 3��������֧��
	$ git branch test


	$ git branch
		* br-2.1.2.2
  			master
  			test
	 �ѷ�֧���͵�Զ�̷�֧
		$ git push origin test
## 4���л�����֧test

	$ git branch
		* br-2.1.2.2
  		master
  		test

		M ��ʾcong ԭ����֧����һ���޸�û���ύbr-2.1.2.2�����������޸�
		$ git checkout test
		M       jingwei-server/src/main/java/com/taobao/jingwei/server/service/cmd/GetCustomerTarCmd.java
		M       jingwei-server/src/main/java/com/taobao/jingwei/server/util/ServerUtil.java
		Switched to branch 'test'

	$ git branch
  		br-2.1.2.2
  		master
		* test
## 5��ɾ�����ط�֧
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
## 6���鿴���غ�Զ�̷�֧  -a��ǰ���*�ŵĴ����㵱ǰ����Ŀ¼�����ķ�֧
    remotes/origin/HEAD -> origin/master #ɶ��˼�أ�  
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

## 7��ɾ��Զ�̰汾
	git push origin :br-1.0.0  
## ɾ��Զ�̷�֧  
### git branch -r -d origin/branch-name  
### git push origin :branch-name 