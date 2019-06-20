
# 多个commit合并成一个commit

开发一个完整功能的过程中可能会有多次提交，当开发完成之后可以将中间的多次提交合并成为一个提交节点，作为这个功能的节点。

通过`git rebase -i`可以将多个commit合并成为一个commit

## 用法

```
git rebase -i commitId
```

## 示例

比如现在的提交如下所示

```
commit f23bc88
第三次提交

commit abb992
第二次提交

commit bc33ad
第一次提交
```

现在将第二次和第三次提交合并为一个提交

1. 输入命令

	```
	git rebase -i bc33ad
	```

	`bc33ad`是第一次提交的commitId,表示对从这次commit之后的commit进行处理

2. 进入交互页面,如下所示

  ```git
  pick abb992 第二次提交
  pick f23bc88 第三次提交
  
  # Commands
  # p, pick <commit> = use commit
  # r, reword <commit> = use commit, but edit the commit message
  # e, edit <commit> = use commit, but stop for amending
  # s, squash <commit> = use commit, but meld into previous commit
  # f, fixup <commit> = like "squash", but discard this commit's log message
  # x, exec <command> = run command (the rest of the line) using shell
  # b, break = stop here (continue rebase later with 'git rebase --continue')
  # d, drop <commit> = remove commit
  # l, label <label> = label current HEAD with a name
  # t, reset <label> = reset HEAD to a label
  
  ```

  可以看到会有一些命令可以操作，常用有下面几个

  pick , 使用这个提交
  reword , 使用这个提交，但是重新编辑提交信息
  squash , 使用这个提交，但是将这个提交合并到上一个提交中
  fixup , 和squash命令差不多，但是不使用提交信息
  drop , 移除这个提交

3. 进行更改
  
  ```
  pick abb992 第二次提交
  squash f23bc88 第三次提交
  ```

  将第三次提交输入命令`squash`,表示将第三次提交合并到第二次提交。

  保存退出之后会进入一个message编辑页面，重新输入message之后就完成了commit合并的操作。

