
# 命令行的配置指导

## 工具安装下载

1. 下载iTerm2

	iTerm2比自带终端功能更加丰富。支持分屏、字体配置、背景配置、快键键等功能

	下载地址：https://www.iterm2.com/

2. 启动iTerm2 更改shell为zsh

	默认的shell为bash

	更改为zsh 

	```
		chas -s /bin/zsh
	```

	为什么要用zsh

3. 下载`oh-my-zsh`

	`oh-my-zsh`是一个对zsh进行配置的开源库。通过这个库可以更方便的配置zsh

4. 更改`.zshrc`进行自定义配置

	添加插件，在`.zshrc`中找到`plugin`字段，在括号中添加要使用的插件

	```
		plugin(git, zsh-autosuggestions)
	```

	更改主题，在`zshrc`中找到`theme`字段，

	```
		theme=muse
	```

***

## 我的当前配置

### 主题

theme=`muse`

### 当前使用的插件

`zsh-autosuggestions`
