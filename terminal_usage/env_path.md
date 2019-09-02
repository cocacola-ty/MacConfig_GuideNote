
# MAC环境变量的配置

## 环境变量的作用

当用户在终端中输入某命令之后，系统会根据`PATH`中的路径去查找是否有可执行文件可以来执行这个命令

比如默认的环境变量是

```
	echo $PATH

	>>> /usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

当执行`node`命令时

系统就会根据当前的环境变量中路径：`/usr/local/bin`、`/usr/bin`、`/bin`、`usr/sbin`、`sbin`。去这些目录下面查找是否存在可执行文件来执行这个命令

当查找到`/usr/local/bin`目录，找到名字为`node`的可执行文件。

执行该`node`文件,启动`node`

_可以理解为环境变量就是命令的搜索路径_

所以，当有新增加的软件环境，比如`python`、`ruby`等，需要将新增加的软件环境的目录添加到系统环境变量`PATH`中。这样当执行对应的命令时，才能在指定的目录找到该命令。

## 配置环境变量

当有新增加的软件环境，如何增加到系统环境变量中。

1. 如果只是临时使用 

	在终端中输入

	```shell
		export 
	```

2. 加入到终端的配置文件中

	终端每次启动时都会先加载终端的配置文件。当命令行使用的是`zsh`时，会先加载`.zshrc`文件。

	所以可以在该文件中新增环境变量

	```shell
		export PY_PATH = /usr/local/bin/python
		export PATH = $PATH:$PY_PATH
	```



