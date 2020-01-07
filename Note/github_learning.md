### 设置用户名和邮箱
```shell
git config --user.name ""
git config --user.email test@163.com
```
### linux常用命令（待学习）
```shell
e: #进入e盘
cd git 进去文件git
```
### git命令
```shell
git status #状态
git checkout   #暂存恢复为原来
git reset file  #提交的恢复为暂存的版本
git add LICENSE
git commit -m "change LCENSE"
git log #查看历史

HEAD 指针
git reset HEAD~~ #指针指向暂存区域，并修改暂存区域内容
git reset --soft HEAD~ #移动HEAD的指向 不修改暂存区域内容 相当于撤销commit命令
git reset --hard HEAD~ #威胁 将暂存区域还原到工作目录
git reset id号 #回滚快照 指针不变

rm test.php
git rm test.php #删除文件
git commit -m""

git push #向github发起请求
```
### github报错：The file will have its original line endings in your working directory

#### 问题描述：
git add：添加至暂存区，但并未提交至服务器。git add . 是表示把当前目录下的所有更新添加至暂存区。有时在终端操作这个会提示：
```shell
warning: LF will be replaced by CRLF in ball_pool/assets/Main.js.
The file will have its original line endings in your working directory
```

#### 原因：
这是因为文件中换行符的差别导致的。这个提示的意思是说：会把windows格式（CRLF（也就是回车换行））转换成Unix格式（LF），这些是转换文件格式的警告，不影响使用。

git默认支持LF。windows commit代码时git会把CRLF转LF，update代码时LF换CRLF。

#### 解决方法：
```shell
git rm -r --cached .
git config core.autocrlf false
git add .
git commit -m ''
 
git push
注：  . 为文件路径名
```

