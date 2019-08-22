
# 命令行的配置指导

## 工具安装下载

1. 下载iTerm2

	iTerm2比自带终端功能更加丰富。支持分屏、字体配置、背景配置、快键键等功能

	下载地址：https://www.iterm2.com/

	**为什么要使用iTerm2**

	iTerm2相比于系统自带的终端可以提供更多的功能。如分屏、字体主题配置、快键键配置等等。

	更改iTerm2的主题

2. 启动iTerm2 更改shell为zsh

	默认的shell为bash

	更改为zsh 

	```
		chas -s /bin/zsh
	```

	**为什么要用zsh**

	bash、zsh、tcsh都是shell。shell就是命令的执行环境

	bash是最通用，最常见的shell，是很多Linux发行版的标配

	zsh通过配置之后可以支持更改功能，如命令自动补全、高亮显示、拼写检查等。

3. 下载`oh-my-zsh`

	`sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

	`oh-my-zsh`是一个对zsh进行配置的开源库。通过这个库可以更方便的配置zsh

4. 添加常用功能插件

	1. 添加`git`插件

	该插件提供了一系列git操作的简化别名。如`gst = git status`、 `gaa = git add` 等

	这个插件是安装`oh-my-zsh`之后就会提供的插件，可以直接使用

	在`.zshrc` 文件中找到`plugins`,在该字段中添加`git`。如下所示

	```
		plugins=(git)
	```

	2. 添加`pod`

	这个插件也是oh-my-zsh默认已经下载好了

	```
		plugins=(
			git 
			pod
		)
	```

	3. 安装`z` 快捷路径跳转插件

	`z`插件是路径快捷跳转，可以直接跳转到指定目录，并且可以自动提示原来使用过的路径

	```
		plugins=(
			git
			pod
			z 
		)
	```

	4. 安装`zsh-autosuggestions` 命令提示插件

	这个插件不是`oh-my-zsh`自带的插件，需要自己去下载才能使用

	下载插件并放到`oh-my-zsh`的插件目录下 

	```
        git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
	```

	在`zshrc`中启用该插件

	```
		plugins=(
			git 
			zsh-autosuggestions
		)
	```

	_这里可以查看`oh-my-zsh`提供了哪些插件 https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins-Overview_

5. 更改主题，在`.zshrc`中找到`theme`字段，

	```
		theme=muse
	```

	**更多主题下载和使用**

	`oh-my-zsh`会自带很多的主题配色。可以在`.oh-my-zsh/themes`目录下查看

	https://github.com/robbyrussell/oh-my-zsh/wiki/External-themes

6. 更多的自定义配置

	https://github.com/robbyrussell/oh-my-zsh/wiki/Customization

***

## 我的当前配置

### 主题

theme=`muse`

### 当前使用的插件

* `zsh-autosuggestions`

* `git`

* `pod`

* `z`
