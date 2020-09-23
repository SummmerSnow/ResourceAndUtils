### Mac 终端显示git分支名称
思路： Mac终端集群默认下是不显示分支名称的，如果想要显示需要修改配置文件，而Mac下默认配置文件为：.bash_profile
solution: 在 .bash_profile 文件下添加如下代码
```
function git_branch { 
  branch="`git branch 2>/dev/null | grep "^\*" | sed -e "s/^\*\ //"`" 
  if [ "${branch}" != "" ];then 
    if [ "${branch}" = "(no branch)" ];then 
      branch="(`git rev-parse --short HEAD`...)" 
    fi 
    echo " ($branch)"
  fi
}
export PS1='\u@\h \[\033[01;36m\]\W\[\033[01;32m\]$(git_branch)\[\033[00m\] \$ '
```
需要 执行 source ~/.bash_profile 使得命令生效。


### 修改用户名和邮箱
$ git log 查看历史提交信息，可以看到历史用户名和密码
查看用户名和密码：
$ git config user.name
$ git config user.email   

修改用户名和密码：
$ git config --global user.name "username"
$ git config --global user.email "email"


### 远程分支强制覆盖本地代码
方案一：
git fetch --all
git reset --hard origin/branchName
git pull

方案二：
从远程origin仓库中的master分支下载到本地分支，并新建一个 temp 分支。
git fetch origin master:temp

## fetch vs. pull 



