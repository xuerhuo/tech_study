# Git


## Git客户端
- PC端
  - [SmartGit](https://www.syntevo.com/smartgit/) 
  - [Sourcetree](https://cn.atlassian.com/software/sourcetree)   ***推荐免费***
- 手机端 
  - Grape For GitHub


![avatar](https://github.com/sanwancoder/it_study_lib/blob/master/images/GrapeForGitHub.png?raw=true)



## Gitflow

### 流程图

![avatar](https://github.com/sanwancoder/it_study_lib/blob/master/images/git-flow-nvie.png?raw=true)


### Git-flow项目

- [https://github.com/nvie/gitflow](https://github.com/nvie/gitflow) ***SourceTree已经集成git-flow***


## Git学习资料

- [廖雪峰 Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)
- [Learn Version Control with Git](https://www.git-tower.com/learn/git/ebook/cn/command-line/introduction#start)
- [git命令](https://git-scm.com/docs)
-[https://learngitbranching.js.org/](https://learngitbranching.js.org/)

## GitHub使用秘籍
  - [GitHub秘籍](https://github.com/tiimgreen/github-cheat-sheet/blob/master/README.zh-cn.md) 




## Git命令

### 关联远程分支
```
 1. echo "# first repo" >> README.md
 2. git init
 3. git add README.md
 4. git commit -m "first commit"
 5. git remote add origin https://github.com/zhangsan/zhangsan_first_repo.git
 6. git push -u origin master
```
### 对于已经存在的仓库 关联
```
git remote add origin https://github.com/zhangsan/helloworld.git
git push -u origin master
```

### git commit 但是没有使用git push，现在发现有文件误提交了
```
        1. git log  找到你想撤销的commit_id

        2.  git reset --hard commit_id 完成撤销,同时将代码恢复到前一commit_id 对应的版本。

        3. git reset commit_id 完成Commit命令的撤销，但是不对代码修改进行撤销，可以直接通过git commit 重新提交对本地代码的修改。
```
### 分支管理
```
1. 切换到远程分支
git checkout -b dev origin/dev，作用是checkout远程的dev分支，在本地起名为dev分支，并切换到本地的dev分支
2. 本地切换分支
git checkout master  切换到master分支
```

### 标签管理
```
1. 打标签
git tag -a v0.1 -m "version 0.1 released" 1094adb  作用: 给 1094adb 这次提交打上标签v0.1 备注是version 0.1 released
2. 远程推送标签
git push origin --tags
3. 显示已有的标签
git tag
git show v1.4


```
[Git-scm 6 Git 基础 - 打标签](https://git-scm.com/book/zh/v1/Git-%E5%9F%BA%E7%A1%80-%E6%89%93%E6%A0%87%E7%AD%BE)

## 好文
- [Git 在团队中的最佳实践--如何正确使用Git Flow](https://www.cnblogs.com/wish123/p/9785101.html)

## 疑难问题解决
  - [mac下git命令行乱码问题解决](https://blog.csdn.net/happycodefly/article/details/88385140)
  

  
