# sublime text 3的配置

## 安装`Package Control`

`Package Control`是sublime text 的插件管理工具.https://packagecontrol.io/installation#st3

执行下面的代码就会安装`Package Control`

```
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by) 
```

## 主题字体配置

### 主题配色安装

1. `cmd + p` 调出`package control`
2. 输入`Package Control: Install Package`
3. 搜索主题。如`Meterial Theme`

color theme : material theme. https://packagecontrol.io/packages/Material%20Theme

### 激活使用主题

1. 进入偏好设置，快捷键`cmd + ,`。 这个配置文件是一个json。在`Preferences-sublime-settings -- User`文件中进行主题配置。

```
{
	"color_scheme": "Packages/Material Theme/schemes/Material-Theme.tmTheme",
	"font_face": "Monaco",
	"font_size": 12,
	"ignored_packages":
	[
		"Vintage"
	],
	"material_theme_accent_sky": true,
	"material_theme_bullet_tree_indicator": true,
	"theme": "Material-Theme.sublime-theme"
}
```

### 字体字号配置

1. 同样在`Preferences-sublime-settings -- User`文件中添加下面配置

```
{
	"font_face": "Monaco",
	"font_size": 12,
}
```

## 代码补全支持

1. `cmd + p` 输入 `Install Package`

2. 搜索`SublimeCodeIntel` 安装

3. 安装完成后打开插件配置。`Preference` - `Package Settings` - `SublimeCodeIntel` - `Setting - User`。如图所示位置

![https://github.com/cocacola-ty/Images/blob/master/sublime_codeintel_config.png?raw=true]

添加如下内容

```
{
	"codeintel_language_settings": {
		"Python3": {
			"python3": "/usr/local/bin/python3",
			"codeintel_scan_extra_dir": [
				"/usr/local/Cellar/python/3.7.1/Frameworks/Python.framework/Versions/3.7/lib/python37.zip",
				"/usr/local/Cellar/python/3.7.1/Frameworks/Python.framework/Versions/3.7/lib/python3.7", 
				"/usr/local/Cellar/python/3.7.1/Frameworks/Python.framework/Versions/3.7/lib/python3.7/lib-dynload",
				"/Users/fengtianyu/Library/Python/3.7/lib/python/site-packages",
				"/usr/local/lib/python3.7/site-packages",
				"/usr/local/lib/python3.7/site-packages/cmd-0.1-py3.7.egg"
			],
			"codeintel_scan_files_in_project": true,
			"codeintel_selected_catalogs": []
		},
	}
}
```

`python3`对应的是Python3环境的路径。 在命令行中通过`which python3`可以查看该路径位置。

`codeintel_scan_extra_dir`是Python的包内容。可以通过如下方式获取这些路径。

1. 进入idle
2. import sys
3. print(sys.path)



