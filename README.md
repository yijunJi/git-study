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