## 常用命令
```
git clone url	//克隆远程仓库
git checkout 	//切换分支
git diff		//查看当前变更
git add .		//暂存要提交的文件
git status		//查看当前状态
git commit -m message	//提交代码
git pull 		//拉取代码
git push		//推送到远程仓库
git merge branchName	//合并分支
git checkout -b branchName	//创建本地分支
git branch -d branchName	//删除分支
git stash		//储藏
git stash list	//查看储藏纪录
git stash apply	//启用储藏目录，可以指定名称
```

$  git checkout -b feature-branch    //创建并切换到分支feature-branch  <br/>
$  git push origin feature-branch:feature-branch    //推送本地的feature-branch(冒号前面的)分支到远程origin的feature-branch(冒号后面的)分支(没有会自动创建)


Git鼓励大量使用分支：
查看分支：git branch
创建分支：git branch <name>
切换分支：git checkout <name>
创建+切换分支：git checkout -b <name>
合并某分支到当前分支：git merge <name>
删除分支：git branch -d <name>
删除远程分支：git push origin --delete <branch-name>

git 合并 commit 教程
https://www.cnblogs.com/wangiqngpei557/p/5989292.html



##### git 将本地文件推送到Github远程仓库<br/>
1. 先在github上创建一个项目：例如 vue-demo<br/> 
2. 在本地vue-demo 项目中使用 git init 把其变成git可以管理的仓库<br/>
`git init`
3. 若要忽略本地的文件或文件夹不被提交到github ，则需要在项目根目录下创建    .gitignore 文件<br/>
`touch .gitignore`
4. 打开文件，编辑内容，例如：<br/>
```
node_modules/ 
update.txt
```
则可以忽略目录下node_modules 文件夹及updata.txt 文件.<br/>
配置文件可以在github在线浏览<br/>
5. 添加文件夹下所有文件到暂存区 git add .<br/>
`git add .`
6. 把文件提交到仓库 git-commit -m “”<br/>
`git commit -m 'decriptions'`
5. 关联远程仓库 （第一次使用需要添加github公钥）<br/>
`git remote add origin git@github.com:***/vue2.1-sell.git`<br/>
或者<br/>
`git remote add origin https://github.com/***/vue2.1-sell.git`
6. 获取远程库与本地同步（远程仓库不为空需要这一步）<br/>
`git pull --rebase origin master`
7. 把本地内容推送到远程库 使用 git-push<br/>
`git push -u origin master`
