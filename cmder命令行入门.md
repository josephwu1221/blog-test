### 命令缩写
|   英文    | 缩写命令 |  英文  | 缩写命令 |
| :-------: | :------: | :----: | :------: |
|   file    |          |  link  |    ln    |
|   make    |    mk    |  find  |   find   |
|   move    |    mv    |  echo  |   echo   |
|  remove   |    rm    | touch  |  touch   |
|   copy    |    cp    | change | cd中的c  |
|   list    |    ls    |  cde   | cd中的d  |
| recursive |          | force  |          |
### 救命快捷键
>任何问题，火速**ctrl+c**中断
如果不小心作死输入`rm -rf`清除盘
###增 删 改 查
#### 查看
+ 查看当前绝对路径
>pwd (*print name of current/working directory*)
+ 查看当前目录内容
>ls (*list directory contents*)【.文件名】，文件名前带点的LS看不见
ls -l，查看更新时间
+ 查看指定目录内容
>ls 路径
+ 查看文件内容  
>cat  路径，显示全部代码
head  路径 ，默认头10行代码，**head XXX -n 14**，看14行
tail  路径，默认尾10行代码，
less  路径，可翻页查看内容，退出输入**q**
#### 增
+ 创建文件
> touch 1.txt,摸一下，没就创建
echo hi > 1.txt  
echo hello >> 1.txt  追加内容
echo -e "1\n2" > 1.txt 输入两行文件内容
+ 创建目录
>mkdir a，创建目录a
mkdir -p a/b/c ，创建多层目录
+ 同时创建多个文件
>touch 1.txt 2.txt
+ 同时创建多个多层目录
>mkdir -p a/b/c /a/d/c
+ 复制文件
> cp 1.txt 2.txt , 复制1.txt黏贴了2.txt
+ 复制目录
把当前目录下的 a 目录复制一份变为 b 目录，怎么写命令?
>cp -r a b , -r 就是 recursive 回归的 递归的
#### 删除
>删除文件 rm 1.txt
删除目录 rm -r a
删除有内容的目录 rm -rf a
####  cd ~ , "~"就是用户目录
#### 修改内容
> code 1.txt ,会打开vscode
start 1.txt , 会**默认程序**打开
echo ' ' > 1.txt，清空内容
#### 移动
>mv 1.txt git-demo-1/ ，移动1.txt到 git-demo-1文件夹
mv git-demo-1/1.txt . ,点就是当前目录
#### 改名
>mv 1.txt 2.txt ，修改了名字1变成2
#### &&操作
当一条命令**成功之后**，执行下一条命令
```touch 1.txt && touch 2.txt &&rm 2.txt && echo 成功``` 
#### ; 操作
不管成功失败都执行下一条操作命令
#### 编写执行脚本
创建一个文件，code【文件名】打开。
**chmod +x 一键搞定 , mac上需要这句话给权限**
运行 sh 【路径】执行
建议加shebang（文件里的一句话，可以指定文件用【你指定的】执行）