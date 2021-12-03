# git_github
github 操作笔记

#### 参考链接 https://www.cnblogs.com/flora5/p/7152556.html

* 1.创建SSH Key 
ssh-keygen -t rsa -C "814971663@qq.com"


*  2.接下来到GitHub上，打开“Account settings”--“SSH Keys”页面，然后点击“Add SSH Key”，填上Title（随意写），在Key文本框里粘贴 id_rsa.pub文件里的全部内容。


*  3.验证是否成功，在git bash里输入下面的命令
ssh -T git@github.com

*  4.下面开始设置username和email，因为github每次commit都会记录他们
$ git config --global user.name  "xuming1986"//你的GitHub登陆名
$ git config --global user.email "814971663@qq.com"//你的GitHub注册邮箱

*  5.接下来就是把本地仓库传到github上去，之前在GitHub上建好一个新的仓库是，跳转的页面，完全按照上面的只是操作就可以了。
$ git remote add origin git@github.com:flora0103/example.git    //关联一个远程库命令， git@github.com:flora0103/example.git   这个是自己远程库
git push -u origin master    //关联后,第一次推送master分支的所有内容命令，此后，每次本地提交后，就可以使用命令git push origin master推送最新修改




# git教程  链接https://www.jianshu.com/p/296d22275cdd
## 安装git 
sudo apt-get install git

## 设置Git
$ git config --global user.name  "xuming1986"
$ git config --global user.email "814971663@qq.com"

## 使用Git
从终端（cmd）进入你想要记录内容更改的文件夹里
例如我们进入gittest文件夹
git init

这个文件夹以后的更改就会被记录了。（如果是空文件夹会提示Initialized empty Git repository in /home/yep/code/gittest/.git/，告诉你文件夹为空）

现在我们在文件夹里新建一个文件hello.txt,内容是
print("Hello World")

git add hello.txt

git commit -m "添加了hello.txt"

$ git add file1.txt
$ git add file2.txt file3.txt
$ git commit -m "add 3 files."

## 实现版本回退
print("Hello World")
print("老板是神经病")

git add hello.txt
git commit -m "hello.txt里添加了一句话"

git log
git reset --hard HEAD^

git reset --hard 88d885

git reflog

# GitHub
1.注册账号GitHub官网
2.创建SSH Key
ssh-keygen -t rsa -C "814971663@qq.com"
3.SSH keys
添加key

## 创建仓库
可以看到主页提供了两种和本地仓库关联起来的方式
方法一：
把本地已有的同名Git仓库和GitHub上的仓库关联起来
我们在本地新建了一个名为Gittest的文件夹
cd D:\home\ming.xu\Gittest

将Gittest文件夹设置为Git仓库
添加文件,比如我们新写了一个hello.txt：

git add hello.txt
git commit -m "first commit"


到此为止已经提交到了本地仓库
接下来我们把本地仓库和远程仓库联系起来
git remote rm origin 
git remote add origin git@github.com:xuming1986/git_github.git

添加后，远程库的名字就是origin，这是Git默认的叫法，也可以改成别的，但是origin这个名字一看就知道是远程库
下一步，就可以把本地库的所有内容推送到远程库上
git push -u origin master









