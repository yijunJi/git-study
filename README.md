#   安装 homebrew 
##  配置用户名与email git config --global user.name 和user.email
##  repository 仓库 ls -ah 查看隐藏目录
##  使用命令git add <file>，注意，可反复多次使用，添加多个文件；
##  使用命令git commit -m <message>，完成。 这里message可以让别人查看到改动
##  git status查看状态
##  git diff查看修改
##  git log 查看修改日志
##  HEAD表示当前版本，HEAD^表示上一个版本 HEAD^^上上版本 HEAD~n前n个版本
##  git reset --hard 版本 表示修改回退，退回想取消，则需要使用git reset --hard id
##  git reflog  记录每一次使用git的命令，方便回滚
##  通过git add才能方便把修改存入咱暂存区
##  git diff HEAD --README.md 查看工作区与版本库的区别
##  git checkout -- file可以将文件回到最近一次git add 或git commit状态
##  命令git reset HEAD <file>可以把暂存区的修改撤销掉（unstage），重新放回工作区：
##  要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
##  关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
##  此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；
##  git checkout -b dev 表示创建并切换到一个新的分支dev  也可以使用git switch -c <name>创建切换
##  git branch 查看当前分支
##  切换后改变内容都在dev分支，切换回master分支的内容不会改变
##  合并分支，切换回master分支后，使用git merge dev 将dev与master分支合并
##  git branch -d dev 删除dev分支
##  git log --graph 查看分支合并图
##  git stash 把当前工作现场“储藏”起来，等以后恢复现场后继续工作
##  使用git stash list查看储存的工作，使用git stash apply 或者git stash pop区别是，后者list中会删除，储存多个的时候git stash apply stash@{0}命令
##  cherry-pick id把某个改动复制到当前分支
##  丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除
##  git remote查看远程仓库信息 git remove -v详细信息

#  因此，多人协作的工作模式通常是这样：
## 首先，可以试图用git push origin <branch-name>推送自己的修改；
## 如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；
## 如果合并有冲突，则解决冲突，并在本地提交；
## 没有冲突或者解决掉冲突后，再用git push origin <branch-name>推送就能成功！

## git tag 标签名 当前版本打标签，回滚或者其他操作室方便查找使用
## 给之前版本打标签git tag 标签名 id 
## git show <tagname>查看标签信息
## $ git tag -a v0.1 -m "version 0.1 released" 1094adb 标签添加说明-a