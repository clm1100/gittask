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