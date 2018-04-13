Git is a distributed version control system.
Git is free software distributed under the GPL.
代码：
1. pwd 显示当前目录
2. git init 将目录变成git管理仓库
3. git add readme.txt 添加到暂存区
   git commit -m "write a readme file" 提交文件
4. git status 掌握仓库运行状态
5. git diff readme.txt 查看修改内容
6. git log 查看提交日志
   git reflog 查看最近的日志，回到最新版本
7. git reset --hard HEAD^ 回到上一版本
                          '^^'表示上上版本,'HEAD~100'表示上100版本
   git reset --hard 75d8c08 回到这个ID的版本
   
   
