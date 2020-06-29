#### 配置SSH 和 获取公钥
```
ssh-keygen -t rsa -b 4096 -C 你的邮箱
cat ~/.ssh/id_ras.pub // 得到公钥内容
id_ras //这是私钥
id_ras.pub //这是公钥
```
去github网站添加公钥，*不是私钥，私钥不给人看
#### 链接线上代码库
`ssh -T git@github.com `
链接github，看到【HI你的用户名就成功了】
`git remote add origin git@xxxxxxx01`
在本地库中打这句，链接你的GITHUB的网上库
#### 链接多地线上代码库
`git remote add origin2 git@xxxxxxx02`
在本地库中打这句，链接你的GITHUB的网上库
`git remote add origin3 git@xxxxxxx03`
在本地库中打这句，链接你的GITHUB的网上库
传好后记得`git push -u origin master`&`git push -u origin2 master`
你也可以上传到腾讯的coding.net去
#### 上传
`git push -u origin master` 推到origin仓库的master分支
`git push origin master:master` **此方法无需git checkout master再推**

#### 如果创建了额外的分支
`git branch x ; git checkout x`; 做了更改分支要保存它，**也要push到线上库** `git push -u origin x`
#### 杀手锏
`git push -u origin 分支名 -f` -f 强制上传
#### 下载(*clone*)
`git clone git@?/xxx.git` 在当前目录创建xxx的目录
`git clone git@?/xxx.git aaa` 在本地新建aaa的目录，记得cd aaa
`git clone git@?/xxx.git .` 在当前目录开库，**一定要是个空目录**
#### 在VScode里打开远程仓库
在终端里安装插件
`yran global add git-open`
用`git open` *打开GitHub远程远程仓库首页*