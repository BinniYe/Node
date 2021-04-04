# Git指令  
  * 配置指令  
    * git config --global user.name "binni"  
    * git config --global user.email binniye@163.com  
    * git config --list --show-origin  
  * 设置别名  
    * git config --global alias.ci commit
    * git config --global alias.last 'log -1 HEAD'
  * 初始化本地库  
    * cd localRepostoryFilder  
    * git init
  * 克隆远程库到本地库，可以指定本地库的文件夹名，也可以指定远程库的名字（默认origin）  
    * git clone https://gitee.com/binniye/note.git
    * git clone https://gitee.com/binniye/note.git folderName  
    * git clone https://gitee.com/binniye/note.git -o github(origin)
  * 查看远程库  
    * git remote
    * git remote -v  
  * 关联远程库到本地，可以同时指定一个方便的简写，默认origin  
    * git remote add url
    * git remote add shortName url  
  * 重命名和删除远程仓库  
    * git remote rename curName newName
    * git remote remove shortName  
  * 拉取远程库所有数据到本地库，不合并到工作区  
    * git fetch origin  
  * 合并新分支到当前分支，即部署新功能  
    * git merge newBranchName
    * git branch -d newBranchName  //新分支部署后，就可以删除了
    * git branch -D hasChangedBranch  //删除有改变的分支，需要强制删除
  * 拉取远程库分支数据到本地库对应的分支，自动合并  
    * git pull  
    * git pull  --rebase
  * 推送当前分支到远程库对应的分支  
    * git push origin master  
    * git push --set-upstream origin master
  * 隐藏、查看、显示修改  
    * git stash
    * git stash list
    * git stash pop  
  * 变基，rebase：将提交到某分支的所有改动都移至另一分支上
    * git checkout curBrach //第一步先找到当前分支
    * git rebase master  //第二步将curBranch变基到master基底，master快进合并
  * 跟踪文件  
    * git add fileName
    * git add .
  * 暂存修改  
    * git add fileNameModified
  * 提交暂存或修改的文件到本地库  
    * git commit -m "[Note][feature]:Create local repository"
    * git commit -a -m "message"
  * 修正提交  
    * git commit -m "message"
    * git add forgottenFileName
    * git commit --amend  
  * 撤销暂存文件，修改的内容不撤销  
    * git reset HEAD fileNameModified  
  * 撤销对文件的修改  
    * git checkout -- fileNameModified
  * 查看状态  
    * git status
    * git status -s
    * git diff  
  * 重命名文件  
    * git mv fileFrom fileTo  
  * 删除文件  
   * git rm
   * git rm --cached fileName  
  * 查看提交历史  
    * git log
    * git log -p -2
    * git log --stat
    * git log --pretty=oneline
    * git log --pretty=format:"%h %s" --graph
    * git log --since="2020-1-13"  

# Git分支  
  * HEAD: 当前所在的分支  
  * 创建分支引起的HEAD变化  
    * git branch newBranchName //创建新分支，HEAD还在当前分支
    * git checkout newBranchName  //切换的新分支，HEAD指向新分支  
    * git branch -b newBranchName  //创建新分支，同时切换到该新分支
  * 查看历史分支  
    * git log --online --decorate --graph --all  
  * 关联本地库分支和远程库分支  
    * git checkout -b name origin/name  //本地库的name分支和远程库name分支建立关联
    * git checkout -b localName origin/remoteName  //关联名字不同的两个分支  
  * 复杂的变基：取出client分支，找到它从server分支分歧后的补丁，把这些补丁应用于master  
    * git rebase --onto master server client
