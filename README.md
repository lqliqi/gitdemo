Git 教程
=======
















# 添加远程库
第1步：创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：

$ ssh-keygen -t rsa -C "youremail@example.com"
## 你要把邮件地址换成自己的邮件地址 ，然后一路回车 , 顺利的话你可以在你电脑的主目录 通过命令
$ cd ~.ssh
里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。

第2步：登陆GitHub，打开“Account settings”，“SSH Keys”页面：
然后，点“SSH and GPG keys”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容：

点“Add ssh Key”，你就应该看到已经添加的Key：

## 本地仓库关联一个远程库使用命令：git remote add origin git@github.com:liqiqi/gitdemo.git

## 关联后，推送master分支内容：git push -u origin master