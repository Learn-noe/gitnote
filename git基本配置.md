## 到官网下载git https://git-scm.com/ 随意选择安装地址，然后一路下一步进行安装
## 初始化Git
### 1.确定git仓库
#### 自定义git项目安装位置，推荐：安装至www目录下
### 2.git初始化
#### 进入www目录下，右键空白处选择git bach,进入git命令行输入git init ，此时，git目录下会生成。git文件（隐藏）
### 3.设置git用户和邮箱
#### 继续在命令行输入 git config --global user.name '你的名字'
####               git config --global user.email '你的邮箱'
## 生成并部署SSH key
### 生成ssh公钥 输入以下命令
#### ssh-keygen -t rsa -C '你的邮箱' 按照以下提示按下三次回车即可
#### 找到公钥 C:\Users\admin 并且用编译工具打开public key：cat ~/.ssh/id_rsa.pub
#### 进入你的github在ssh key里面添加你的cat ~/.ssh/id_rsa.pub 里的内容# ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC6eNtGpNGwstc....
## 项目文件获取
### 1.clone 项目文件（首次部署项目）
#### 进入www目录，右键空白处选择git bash，命令行输入git clone git@你的项目地址，此时www目录下会生成‘你的项目’文件夹，包含线上项目文件 注意：#如果获取项目文件失败，请关闭window防火墙后重试
### 2.（之后更新获取文件）提交代码前要更新项目文件因为不止你一个人在开发，你会覆盖其他人已经修改的文件
#### 输入git pull 或者git pull git@你的项目地址，此时会获取最新项目代码
### 3.上传项目 git add 你的文件 记住要加后缀 文件姐不用
### 4.git commit -m '你更新文件的说明'
### git push上传文件