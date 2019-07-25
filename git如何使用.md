#git如何使用
## 本地项目文件如何上传和github关联
- 在文件的根目录执行： git init
- 将本地文件进行提交： git add .（.表示提交全部文件）
- 将add的文件commit： git commit -m "第一次提交"
- 在github上创建一个项目
- 将本地项目和github项目关联起来 git remote add origin https://github.com/YOUNGEER/iOS_learn.git
- 将远程代码拉取到本地：git pull --rebase origin master
- 将本地代码提交到远程：git push -u origin master
