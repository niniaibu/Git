Git is a distributed version control system.
Git is free software distributed under the GPL.
代码：
1. pwd 显示当前目录

2. git init 将目录变成git管理仓库

3. git add readme.txt 添加到暂存区
   git commit -m "write a readme file" 提交文件

4. git status 掌握仓库运行状态

5. git diff readme.txt 查看修改内容
   git diff HEAD -- readme.txt 查看工作区和版本库最新版的区别

6. git log 查看提交日志
   git reflog 查看最近的日志，回到最新版本

7. git reset --hard HEAD^ 回到上一版本
                          '^^'表示上上版本,'HEAD~100'表示上100版本
   git reset --hard 75d8c08 回到这个ID的版本
   git reset HEAD readme.txt 把暂存区的修改回退到工作区

8. git checkout -- readme.txt 文件在工作区的修改全部撤销（1：撤销和版本库一样，2：撤销和暂存区状态一样）

9. cat readme.txt 查看文件内容


提交SSH Key到GitHub
ssh-keygen -t rsa -C "1017578983@qq.com"
点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容   
   
   
