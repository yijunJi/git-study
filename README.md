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