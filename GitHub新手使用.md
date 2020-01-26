**GitHub[^1]新手使用**

1. 注册GitHub账号

2. 创建自己的仓库

3. 安装Git Bash(git-scm.com，下载过程中直接默认选项即可)

4. Git Brash 命令

   1. 在本地创建ssh key
      + ssh-keygen-t rsa-C "your_email@youremail.com[^2]"
      + ![img](https://img-blog.csdn.net/20170912222716512?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvSGFuYW5pX0ppYQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)
      + 进入存储位置打开.ssh文件夹，找到id_rsa.pub打开，复制其中密匙并粘贴到GitHub设置界面的"SSH GPG keys"选项
   2. 检查是否成功绑定
      + ssh -T git@github.com
      + 第一次绑定时输入以上代码会提示是否continue，输入yes后出现：You've successfully authticated,but GitHub does not provide shell access.则说明已经成功连接GitHub。
   3. 后续设置
      + git config --global user.name "your name"
      + git config --global user.email "your_emial@youremail.com"
   4. 将GitHub的库克隆下来到本地电脑中
      - 在自己所选择的文件存储位置打开Git Brash Here，Git Brash会自动定位到该位置
      - git clone 仓库网址(.git)
   5. 上传
      + 在此目录下写入文件，并将git定位到此目录(可用ls查看所定位的文件)
      + git clone 仓库网址(.git)
      + git add test.txt(add .  ：添加全部文件)
      + git commit -m "备注"
      + git push origin master
      + ![图片](https://img-blog.csdn.net/20170912224136180?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvSGFuYW5pX0ppYQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)
      + 在这里登录之前注册的GitHub账号后点击login

5. 非第一次登录使用

   + git add

   + git commint -m " "

   + git push origin master

     



[^1]:代码托管平台
[^2]:注册Github时绑定的邮箱账号

