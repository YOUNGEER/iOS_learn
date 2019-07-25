# git如何使用

## 本地项目文件如何上传和github关联
- 在文件的根目录执行： git init
- 将本地文件进行提交： git add .（.表示提交全部文件）
- 将add的文件commit： git commit -m "第一次提交"
- 在github上创建一个项目
- 将本地项目和github项目关联起来 git remote add origin https://github.com/YOUNGEER/iOS_learn.git
- 将远程代码拉取到本地：git pull --rebase origin master
- 将本地代码提交到远程：git push -u origin master

## git相关命令

- gi t clone 网址：将该网址的内容clone到当前文件目录下
- git log:查看提交的日志
- git status：查看工作目录当前状态的
- git add file /git add . :添加文件/所有文件到git的跟踪中
- git commint -m "提交日志":添加到本地版本控制中
- git push -u origin master：提交到远程版本控制中
- git commint +小写i+“日志”+ESC+连续两次大写Z：commit操作



## head，master和branch

- head：是当前分支的最新的commit的引用，如果当前分支没有commit操作，那么head是当前分支的引用
- master和branch是平等的，只是master是默认创建的分支，clone下来的也是默认master中代码
- branch的创建
  - git branch branch1+git checkout branch1:创建分支branch1，并将head切换到了该分支上
  - git checkout -b branch1:上面的两步简写
  - git branch -d branch1:删除分支branch1，注意，删除的时候head一定不能在该分支上



## push实质

- push：把本地branch的commits提交到远程仓库
- git push -u origin master,这里的origin表示远程仓库，master表示本地的master代码提交到远程仓库的master中
- git checkout branch1+git push origin branch1:切换head到分支branch1，然后提交分支branch1到远程仓库的分支branch1上
- 远程仓库的head永远是指向master的



## merge实质

- pull的本质是fetch代码和再merge代码
- 实质：将目标commit路径上的所有connit的内容一并应用到当前commit上，并自动生成一个新的commit
- 分支合并/同一分支前后合并
- head指向master+git merge branch1:branch1合并到master上



## add

- git add . :add所有文件
- add后再次修改文件，需要重新再add，然后才能再commit



## rebase

- 重新设置基础点
- 要从分支rebase到master才是正确操作
- git checkout branch1+git rebase master





