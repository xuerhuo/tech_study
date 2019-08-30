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

- 关联远程分支
```
 1. echo "# first repo" >> README.md
 2. git init
 3. git add README.md
 4. git commit -m "first commit"
 5. git remote add origin https://github.com/zhangsan/zhangsan_first_repo.git
 6. git push -u origin master
```
- 对于已经存在的仓库 关联
```
git remote add origin https://github.com/zhangsan/helloworld.git
git push -u origin master
```

- git commit 但是没有使用git push，现在发现有文件误提交了
```
        1. git log  找到你想撤销的commit_id

        2.  git reset --hard commit_id 完成撤销,同时将代码恢复到前一commit_id 对应的版本。

        3. git reset commit_id 完成Commit命令的撤销，但是不对代码修改进行撤销，可以直接通过git commit 重新提交对本地代码的修改。
```



## 好文
- [Git 在团队中的最佳实践--如何正确使用Git Flow](https://www.cnblogs.com/wish123/p/9785101.html)

## 疑难问题解决
  - [mac下git命令行乱码问题解决](https://blog.csdn.net/happycodefly/article/details/88385140)
  

  
