# oh-my-zsh 主题的使用

oh-my-zsh可以通过设置主题来显示不同的配色方案

oh-my-zsh主题更改的命令提示符、高亮颜色等

字体、字间距等的更改是需要通过iTerm2来进行配置

## 查看可使用的主题

`oh-my-zsh`会自带很多的主题配色。

自带的主题配色文件都放在`.oh-my-zsh/themes`目录下

这些都是可以使用的配色方案

![zsh_theme_snapview](https://raw.githubusercontent.com/cocacola-ty/Images/master/zsh_theme_snapview.jpg)

## 下载自定义主题

如果需要下载其他的第三方主题配色，可以在github搜索`*.zsh-theme`

下载下来之后放到`.oh-my-zsh/themes`目录下即可

## 更改当前的主题

编辑`.zshrc`，设置`ZSH_THEME`字段的值为选择使用的主题的名字

如`ZSH_THEME=muse`

如果不使用主题配色，将该字段设置为空。`ZSH_THEME=""`

> https://github.com/robbyrussell/oh-my-zsh/wiki/Customization#overriding-and-adding-themes

> https://github.com/robbyrussell/oh-my-zsh/wiki/Themes