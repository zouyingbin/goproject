### **git分支操作**

#### 切换并创建分支

```shell
[zyb@localhost goproject]$ git checkout -b dev
切换到一个新分支 'dev'
[zyb@localhost goproject]$ git branch -a
* dev
  master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
```

#### 推送新分支到远程

```shell
[zyb@localhost goproject]$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/zouyingbin/goproject/pull/new/dev
remote: 
To git@github.com:zouyingbin/goproject.git
 * [new branch]      dev -> dev
```

#### 建立分支关联

```shell
[zyb@localhost goproject]$ git branch --set-upstream-to=origin/dev dev
分支 dev 设置为跟踪来自 origin 的远程分支 dev。
[zyb@localhost goproject]$ git pull
Already up-to-date.
```

#### 分支命令小结

```shell
#删除远程分支命令：

git push origin   :<远程分支名称> 

git push origin --delete <远程分支名称>

#删除本地分支：

git branch -d <本地分支名称>

#查看所有分支:

git branch -a
```



### git提交操作