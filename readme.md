
### 本地仓库初始化连接远程仓库操作：

~~~
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:clm1100/gittask.git
git push -u origin master
//…or push an existing repository from the command line
git remote add origin git@github.com:clm1100/gittask.git
git push -u origin master
~~~



### 推送本地分支local_branch到远程分支 remote_branch并建立关联关系
~~~
a.远程已有remote_branch分支并且已经关联本地分支local_branch且本地已经切换到local_branch

    git push

b.远程已有remote_branch分支但未关联本地分支local_branch且本地已经切换到local_branch

    git push -u origin/remote_branch

c.远程没有有remote_branch分支并，本地已经切换到local_branch

    git push origin local_branch:remote_branch
~~~

### 注意切换分支后 git push 分支时 用的语法是
~~~
git push origin local_branch:remote_branch
~~~

###简写语法为:
####(只有分支名称远程和本地名称一样)
~~~
git push origin test
~~~

之后的操作 add commit 语法何在主分支一样使用;<br>
### 但是需要注意：
//git push 时需要设置在本分支默认提交到远程仓库的分支;如何设置呢？？？<br>
~~~
git push -u origin test 
~~~
//意思是将本地仓库的test分支提交到远程仓库的test分支，
//并默认在此分支下默认git push 就是提交到test分支;


###  将dev分支合并到test分支（开发完，单测后将dev分支代码合并到test分支提测）
#### git merge的基本用法为把一个分支合并到当前分支。

分支合并步骤（将dev分支合并到test分支）

~~~
（1）分支切换,将本地从dev分支切换到test分支: git  checkout test

（2）将本地test分支更新为最新: git pull

（3）将本地dev分支合并到本地test分支: git merge dev

（4）提交本地test分支作为远程的test分支: git push origin  test:test
~~~


在我们合并之前把本地test分支从远程更新为了最新的代码版本，所以这时如果没有人提交新代码到test远程分支，则test本地代码和远程代码是一样的，这时我们在合并本地dev的代码到本地test，这时本地test的代码相比远程就多dev中开发的代码，所以这时我们提交本地test分支作为远程的test分支是正常。

### 常用命令:
#### 查看远程仓库
~~~
git remote -v
~~~
#### 查看本地仓库

~~~
git remote -v
~~~

#### 查看所有仓库


### 关于分支的命令;

#### 查看所有分支包括远程分支
~~~
git branch -a
~~~

### 查看当前分支和本地所有分支
~~~
git branch
~~~
测试行111111111123231

#### 我在clm分支111


#### 本地创建一个分支并推送到远端

- 新建本地分支 git branch clm
- 切换到本地分支 git checkout clm
- 将本地分支推送到远程仓库,并建立远程同名仓库:git push origin clm:clm
- 或者用简单语法: git push origin clm

#### 删除分支
- 删除远程分支 git push origin --delete 远程分支名
- 删除分支 git branch -d 分支名

