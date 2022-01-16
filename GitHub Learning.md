# GitHub Learning

## 基本概念

● Git 仓库

一般情况下，我们可以免费建立任意个 GitHub 提供的 Git 仓库。但

如果需要建立只对特定人物或只对自己公开的私有仓库，则需要依照套

餐类型 B 支付每月最低 7 美元的使用费。



● Issue

Issue 功能，是将一个任务或问题分配给一个 Issue 进行追踪和管理的功能。可以像 BUG 管理系统或 TiDD（Ticket-driven Development）的Ticket 一样使用。在 GitHub 上，每当进行我们即将讲解的 Pull Request，都会同时创建一个 Issue。每一个功能**更改或修正**都对应一个 Issue，讨论或修正都以这个Issue 为中心进行。只要查看 Issue，就能知道和这个更改相关的一切信息，并以此进理.在 Git 的提交信息中写上 Issue 的 ID，GitHub 就会自动生成从 Issue 到对应提交的链接。另外，只要按照特定的格式描述提交信息，可以关闭 Issue。



● Wiki

通过 Wiki 功能，任何人都能随时对一篇文章进行更改并保存，因

此可以多人共同完成一篇文章。该功能常用在开发文档或手册的编写

中。Wiki 页也是作为 Git 仓库进行管理的，改版的历史记录会被切实保

存下来，使用者可以放心改写。由于其支持克隆至本地进行编辑，所以

程序员使用时可以不必开启浏览器。



● Pull Request

开发者向 GitHub 的仓库推送更改或功能添加后，可以通过 Pull Request 功能向别人的仓库提出申请，请求对方合并。

Pull Request 送出后，目标仓库的管理者等人将能够查看 Pull Request 的内容及其中包含的代码更改。

同时，GitHub 还提供了对 Pull Request 和源代码前后差别进行讨论的功能。通过此功能，可以以行为单位对源代码添加评论，让程序员之间高效地交流。



* 版本管理

版本管理就是*管理更新的历史记录*。它为我们提供了一些在软件开发过程中必不可少的功能，例如记录一款软件添加或更改源代码的过程，回滚到特定阶段，恢复误删除的文件等。



**Git 属于分散型版本管理系统，是为版本管理而设计的软件**



## 初始设置

首先来设置使用 Git 时的姓名和邮箱地址。名字请用英文输入。

```
 git config --global user.name "Firstname Lastname"

 git config --global user.email "your_email@example.com"
```



将 color.ui 设置为 auto 可以让命令的输出拥有更高的可读性。

```
 git config --global color.ui auto
```



**设置 SSH Key**

GitHub 上连接已有仓库时的认证，是通过使用了 SSH 的公开密钥认证方式进行的。

```
$ ssh-keygen -t rsa -C "your_email@example.com"
Generating public/private rsa key pair.
Enter file in which to save the key
(/Users/your_user_directory/.ssh/id_rsa): 按回车键
Enter passphrase (empty for no passphrase): 输入密码
Enter same passphrase again: 再次输入密码
```



## 命令行

* **git log** 查看提交日志

如果想查看提交所带来的改动，可以加上 - p参数，文件的前后差别就会显示在提交信息之后。



* **git init**  初始化仓库。成功后会生成 .git 目录，存储着管理当前目录内容所需的仓库数据



* **git status**  用于显示 Git 仓库的状态



* **git add**   向暂存区中添加文件，要想让文件成为 Git 仓库的管理对象，就需要用 git add命令将其加入暂存区（Stage 或者 Index）中。暂存区是提交之前的一个临时区域。



* **git commit**	保存仓库的历史记录

```
$ git commit -m "First commit"

//-m 参数后的 "First commit"称作提交信息，是对这个提交的
概述。
```

如果想要记述得更加详细，请不加 - m，直接执行 git commit命令。

在编辑器中记述提交信息的格式如下:

● 第一行：用一行文字简述提交的更改内容

● 第二行：空行

● 第三行以后：记述更改的原因和详细内容



* **git diff**  	查看更改前后的差别. 可以查看工作树、暂存区、最新提交之间的差别。

查看与最新提交的差别 git diff HEAD



* **git branch**	显示分支一览表

git branch命令可以将分支名列表显示，同时可以确认当前所在分支。

有*代表当前分支为该分支。



删除分支： **git branch -d** 

* **git checkout -b**	创建、切换分支

``````
$ git checkout -b feature-A
//实际上，连续执行下面两条命令也能收到同样效果。
$ git branch feature-A
$ git checkout feature-A
//切换到master分支
git checkout master
//回到上一个分支
git checkout -
``````

 

* **git merge**		合并分支

为了在历史记录中明确记录下本次分支合并，我们需要创建合并提交。因此，在合并时加上 --no-ff参数。

 git merge --no-ff feature-A



* **git log --graph**——以图表形式查看分支

能很清楚地看到特性分支（feature-A）提交的内容已被合并。除此以外，特性分支的创建以及合并也都清楚明了。



* **git reset**——回溯历史版本

    要让仓库的 HEAD、暂存区、当前工作树回溯到指定状态，需要用到 git rest --hard命令。只要提供目标时间点的哈希值 A，就可以完全恢复至该时间点的状态。回到以前的版本。同样也可以返回后面的版本。

    先通过git log或者git reflog查找到以前的版本信息，然后复制其指针指向的号，再 `git reset --hard number`

    

 * **git commit --amend**——修改提交信息

    

 *  **git remote add**——添加远程仓库

    `git remote add origin git@github.com:github-book/gittutorial.git`

    

 * **git clone**——获取远程仓库

    

 * **git pull**——获取最新的远程仓库分支

   
   
 * **git push**  推到远程库

 * **git reflog**    刷新日志，查看版本信息

## 功能

### 分支

git branch	创建分支

git branch -v	查看分支

git checkout	切换分支

git merge	合并到指定分支（在要合并到的分支把将要合并的分支合并过来，后面跟的是要合并的分支）

 

合并冲突问题：同一个位置有不同的方法要合并，无法做出判断，需要人为修改。

查看文件： 

<<<<<<< 当前分支

当前分支代码

`=======` 	

要合并分支代码

`>>>>>>>>>>>`

此时commit后不需要加文件名



### 创建远程仓库

`git remote -v`	查看当前所有远程地址别名

`git remote add 别名 远程地址` 	

### 团队协作

