## 1��Զ�̷�֧���Ǳ��ط�֧push���������ϵ�ʱ������ġ�����master����һ�����͵�Զ�̷�֧��Ĭ�ϣ���
	$ git push origin master
## 2������master֮�����ǻ�������㴴����֧��Ȼ��push����������ȥ ���磺
	$ git push origin develop 
## 3��Զ�̷�֧�ͱ��ط�֧��Ҫ���֣����ԣ��ٴӷ���������ȡ�ض���֧��ʱ����Ҫ�ƶ��ض���֧������
	$ git checkout --track origin/develop 
 /* ע����������--track����������Ҫ��git1.6.4����  ����git�ͻ��Զ��л���develop��֧ */
## 4��ͬ������Զ�̷�֧
	$git fetch origin
## 5���ύ��֧���ݵ�Զ�̷�����
	$ git push origin <local_branch_name>:<remote_branch_name>
	���磺
		$ git push origin develop:develop
	����ڵ�ǰdevelop��֮�£�Ҳ����ֱ��
		$ git push
## 6��ɾ��Զ�̷�֧develop
	$ got push origin :develop
##  ��һ�δ�����ʱ�����������û���κη�֧��ʹ��git init --bare��.��ô�ڱ��ش�����֮����Ҫ����һ����֧�����������档
## ������һ��push��������д git push origin master:master
    git checkout master         //ȡ��master�汾��head��
    git checkout tag_name    //�ڵ�ǰ��֧�� ȡ�� tag_name �İ汾
    git checkout  master file_name  //������ǰ���ļ�file_name���޸�
## git checkout branch_name tag_name //ȡָ����֧branch_name��tag_name�İ汾
## git checkout  commit_id  file_name  //ȡ�ļ�file_name�� ��commit_id�ǵİ汾��
## commit_idΪ git commit ʱ��shaֵ��
## �г�ĳһ��commit ID(XXXXXXXXXXXXXXXX) ��Ӧ�Ĳ�����
   $ git log -1 -p XXXXXXXXXXXXXXXX
   $ git format-patch -1 XXXXXXXXXXXXXXXX <===-1����ʡ��
        --stdout         //��ӡ����׼���
   $ git show XXXXXXXXXXXXXXXX
   $ git diff-tree -p XXXXXXXXXXXXXXXX