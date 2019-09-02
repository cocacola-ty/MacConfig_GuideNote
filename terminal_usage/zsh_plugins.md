# oh-my-zsh插件的安装和使用

## oh-my-zsh自带的插件

oh-my-zsh提供了很多插件可以使用

[这里可以查看提供了哪些插件](https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview)

* `git`

	这个插件提供了一系列的git别名，如`gst` = `git status` 、`gaa` = `git add .` 、 `gcmsg` = `git commit -m ''`

* `z`

	这个插件是快速跳转使用

## 第三方插件的安装

第三方的插件直接将插件下载到插件所在目录`.oh-my-zsh/plugins`。

如`zsh-autosuggestions`插件的下载安装

```
	git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions

```

## 启用插件

在`.zshrc`中找到`plugins`字段，在该字段的值添加要使用的插件的名字。如下所示

```
	plugins = (
		git
		z
		zsh-autosuggestion
	)
```

