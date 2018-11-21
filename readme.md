
### 本地仓库初始化连接远程仓库操作：

~~~
git init<br>
git add README.md<br>
git commit -m "first commit"<br>
git remote add origin git@github.com:clm1100/gittask.git<br>
git push -u origin master<br>
//…or push an existing repository from the command line<br>
git remote add origin git@github.com:clm1100/gittask.git<br>
git push -u origin master<br>
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
简写语法为:
~~~
git push origin test(分支名称远程和本地名称一样)
~~~

之后add commit 语法何在主分支一样使用;
但是需要注意：
git push 时需要设置在本分支默认提交到远程仓库的分支；如何设置呢？？？<br>
git push -u origin test <br>
意思是将本地仓库的test分支提交到远程仓库的test分支；并默认在此分支下默认git push 就是提交到test分支;


~~~
将dev分支合并到test分支（开发完，单测后将dev分支代码合并到test分支提测）
<p>
git merge的基本用法为把一个分支或或某个commit的修改合并到现在的分支上。
<p>
分支合并步骤（将dev分支合并到test分支）

（1）、分支切换： git  checkout test

将本地从dev分支切换到test分支

（2）、将本地test分支更新为最新：  git pull

将本地test分支从远程跟新为最新

（3）、分支合并： git merge dev

将本地dev分支合并到本地test分支

（4）、提交本地test分支作为远程的test分支: git push origin  test:test

在我们合并之前把本地test分支从远程更新为了最新的代码版本，所以这时如果没有人提交新代码到test远程分支，则test本地代码和远程代码是一样的，这时我们在合并本地dev的代码到本地test，这时本地test的代码相比远程就多dev中开发的代码，所以这时我们提交本地test分支作为远程的test分支是正常。

~~~



