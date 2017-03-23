## Git

### 将本地的项目关联到远程仓库

#### 创建的远程仓库有文件
1. `git init` : 初始化git仓库
2. `git add .` : 将文件添加到缓存区
3. `git commit -m"add project"` : 提交文件
4. `git remote add origin xxxx` : 给本地仓库指定远程仓库地址， origin 为远程仓库的名字，xxxx 为远程仓库的地址
5. `git branch --set-upstream-to=origin/master master` : 将远程的master分支设置为本地master分支的上行
6. `git pull --allow-unrelated-histories` : 拉取远程仓库分支的代码，参数 `--allow-unrelated-histories` 的含义[Stackoverflow](http://stackoverflow.com/questions/37937984/git-refusing-to-merge-unrelated-histories)，如果不添加该参数会报错 : `fatal: refusing to merge unrelated histories`
7. `git push` : 将本地代码提交到远程仓库

#### 创建的远程仓库无文件
1. git init 
2. git add .
3. git commit -m"add project"
4. git remote add origin xxxx
5. git push -u origin master : 将本地内容添加到origin仓库

#### 相关命令
* git branch : 显示本地分支 
* git branch -vv : 显示本地分支和对应的远程分支
* git remote -v : 显示远程仓库地址
* git remote rm xxx : 移除远程仓库地址
* git checkout -b xxx : 新建并切换分支
* git checkout : 切换分支
* git merge : 合并分支
