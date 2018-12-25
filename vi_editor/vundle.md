# Vundle的安装和使用

https://github.com/VundleVim/Vundle.vim

## Vundle的安装

1. 将Vundle下载到`~/.vim/bundle/Vundle.vim`目录

```
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

2. 启用Vundle

```
set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

call vundle#end()            " required
filetype plugin indent on    " required
```

将这段代码放在`.vimrc`的开始。就会启用Vundle管理插件

将需要安装的插件写在`begin()`和`end()`之间。如下所示

* 插件是github上的一个库

    ```
    call vundle#begin()
    Plugin 'tpope/vim-fugitive'
    call vundle#end()
    ```

* 插件是其他git地址

    ```
    call vundle#begin()
    Plugin 'git://git.wincent.com/command-t.git'
    call vundle#end()
    ```

* 插件是本地的文件

    ```
    call vundle#begin()
    Plugin 'file:///home/gmarik/path/to/plugin'
    call vundle#end()
    ```

3. 安装插件

    1. 在vim中安装

    启动Vim，运行`:PluginInstall`

    2. 在命令行中安装，执行下面的命令

    ```
    vim +PluginInstall +qall
    ···

***

[vim插件](https://vimawesome.com/)