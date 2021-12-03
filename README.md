# git_github
github 操作笔记

#### 参考链接 https://www.cnblogs.com/flora5/p/7152556.html

## 1.创建SSH Key 
ssh-keygen -t rsa -C "814971663@qq.com"


## 2.接下来到GitHub上，打开“Account settings”--“SSH Keys”页面，然后点击“Add SSH Key”，填上Title（随意写），在Key文本框里粘贴 id_rsa.pub文件里的全部内容。


## 3.验证是否成功，在git bash里输入下面的命令
ssh -T git@github.com

## 4.下面开始设置username和email，因为github每次commit都会记录他们
$ git config --global user.name  "xuming1986"//你的GitHub登陆名
$ git config --global user.email "814971663@qq.com"//你的GitHub注册邮箱

## 5.接下来就是把本地仓库传到github上去，之前在GitHub上建好一个新的仓库是，跳转的页面，完全按照上面的只是操作就可以了。
$ git remote add origin git@github.com:flora0103/example.git    //关联一个远程库命令， git@github.com:flora0103/example.git   这个是自己远程库
git push -u origin master    //关联后,第一次推送master分支的所有内容命令，此后，每次本地提交后，就可以使用命令git push origin master推送最新修改
