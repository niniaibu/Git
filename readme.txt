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

关联远程库
  git remote add origin git@github.com:niniaibu/Git.git   

本地库内容推到远程库
  git push -u origin master 加上-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来
  git push origin master 

克隆到本地库
  git clone git@github.com:niniaibu/gitskills.git

创建分支并合并
1. 创建、切换分支
   git checkout -b dev 加上-b参数表示创建并切换
       相当于：git branch dev （创建）
	           git checkout dev （切换）
   git branch命令会列出所有分支，当前分支前面会标一个*号。
2.两步提交（add、commit）
3.查看分支
   git branch
4.切换分支
   git checkout master
5.合并分支
   git merge dev  合并指定分支到当前分支
6.删除分支dev
   git branch -d dev
   
查看分支合并情况
  git log --graph --pretty=oneline --abbrev-commit

分支管理策略，不使用Fast forward模式
  git merge --no-ff -m "merge with no-ff" dev
  
保存现场  
  git stash
  
恢复并将stash内容删除
  git stash pop
  也即：git stash apply  恢复stash
        git stash drop   删除stash

