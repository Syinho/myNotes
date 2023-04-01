# 当前分支没有上游分支

- 情景复现: 
  - 新建一个文件夹, 
  - 初始化, 
  - git remote add origin [地址] 
  - git add . 
  - git commit -v ''
  - git push

```
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```

调用git push --set-upstream origin master , 不省略的写法应该是git push --set-upstream origin master:master. 即将origin的master分支与本地master分支关联.