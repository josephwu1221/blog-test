需要配置，注意**一行行运行配置**
```
git config --global user.name 名字
git config --global user.email 邮箱
git config --global push.default simple
git config --global core.quotepath false
git config --global core.editor "code --wait"
git config --global core.autocrlf input
```
>上面的英文名和邮箱跟 GitHub 没有关系。
可以跟 GitHub 的用户名和邮箱保持一致，
也可以不一致。我的是一致的。
注意：你需要保证 code 是可以直接在命令行执行的。
如果不能执行，你需要安装 VSCode 并配置 PATH。
### git init
>本地仓库初始化
### git add 【路径】
>选择哪些变动是需要提交的
路径可以是绝对路径 & 相对路径
.和*
### .gitignore
>选择 哪些变动是**不需要**地提交的
比如node_modules
.DS_store
.idea
.vscode
### git commit -m 字符串
>提交，并说明提交理由
字符串里如果**有空格要用""包起来**
### git commit -v
>专业的写代码提交版本注释的方法【推荐】
### git log
>查看记录
### git reflog
>查看版本记录，**包括版本回滚、切换的记录**
### git reset --hard 【版本号】
>**变更版本**
### .gitignore
>不上传的
在文件夹里创建.gitignore，里面写上文件名
被写的文件名的文件不会上传
#### 常用命令
```
git init //不要在已经初始化好的仓库使用，否则会将已经初始化完成的仓库覆盖
git status //查看状态
git status -sb //查看总结
git add //提交文件放入暂存区
git commit  //将暂存区的更新提交到本地仓库
git push origin master //把当前本地仓库里的改动推送到远程仓库（origin）的master分支。之后可以直接git push。
git pull //当远程仓库有变动但是本地仓库没有更新，会拒绝git push， 使用git pull将远程仓库拉到本地仓库，合并变动。
git push -f origin master //强制推送，会覆盖别人的代码
git remote add xxx git@xxx.git //再次添加一个远程仓库的标签
git push xxx master //推送到xxx标签的地址
git remote remove xxx //删除xxx标签
git remote set-url origin url //修改origin标签对应的地址
git remote rename xxx coding //把xxx标签名修改为coding
```
### 创建新的时间线/版本
>**git branch X**，基于当前commit 创建一个新的时间线【分支】
**git checkout **
用于切换另一个分支
当前目录有未提交的代码，只要跟另一个分支不冲突，就没关系，但是reset --hard是影响的！
如果冲突，用**git stash**，也可以合并冲突。
### 版本合并
`git merge 你的branch名字`
提示你解决冲突
修复好冲突，`git add` 后 `git commit` *不需要写文件名
### 删除branch
`git branch -d 分支名`