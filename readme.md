…or create a new repository on the command line<br>
echo "# gittask" >> README.md<br>
git init<br>
git add README.md<br>
git commit -m "first commit"<br>
git remote add origin git@github.com:clm1100/gittask.git<br>
git push -u origin master<br>
…or push an existing repository from the command line<br>
git remote add origin git@github.com:clm1100/gittask.git<br>
git push -u origin master<br>

~~~
4、推送本地分支local_branch到远程分支 remote_branch并建立关联关系

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
