# Git使用时常见问题

* 删除远端分支 / tag

	```
		git push origin --delete <branchName>
		git push origin --delete tag <tagName>
	```

* 对Merge Request节点进行回滚

	对于一般的提交，只有一个父节点，所以当使用`revert`回滚的时候，会将修改内容对于父节点进行回滚修改。

	但是对于Merge Request的提交节点是有两个父节点的。所以当`revert`的时候，需要指定参考的父节点。

	```
		git revert <commitId> -m 1
	```