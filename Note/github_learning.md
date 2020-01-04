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
