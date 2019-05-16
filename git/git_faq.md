# Git使用时常见问题

* ##### 对Merge Request节点进行回滚

	对于一般的提交，只有一个父节点，所以当使用`revert`回滚的时候，会将修改内容对于父节点进行回滚修改。

	但是对于Merge Request的提交节点是有两个父节点的。所以当`revert`的时候，需要指定参考的父节点。

	```
		git revert <commitId> -m 1
	```

## 分支

* ##### 重命名分支

	```
		git branch -m old_branch_name new_branch_name
	```

	修改当前分支名

	```
		git branch -m <new_branch_name>
	```

* ##### 删除远端分支 / tag

	```
		git push origin --delete <branchName>
		git push origin --delete tag <tagName>
	```

* ##### 清理远端已经删除但本地仍然存在的分支

	```
		git remote prune origin
	```

***

## 调研学习

- git分支的`stale`状态是什么意思

- `git gc`怎么使用

- `git prune`怎么使用

- `git remote show origin` 展示的信息