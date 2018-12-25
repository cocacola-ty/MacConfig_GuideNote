# 我的当前vim配置

编辑`~/.vimrc`， 不存在则创建该文件

1. 第一部分为插件，这部分必须要放在开始的位置

2. 基础配置项

## 插件配置项

[Vundle的安装和使用](./vundle.md)

```
" Plugins
set nocompatible
filetype off
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'itchyny/lightline.vim' "状态栏插件

call vundle#end()
filetype plugin indent on
```

添加完插件相关内容之后，在vim中执行`:PluginInstall`安装插件

### 插件的相关配置

### 用到的插件

* `itchyny/lightline.vim` -- 状态栏显示样式插件。地址:https://github.com/itchyny/lightline.vim

## 快捷键配置

* F5键编译运行Python代码

    ```
    map <F5> :call ComplileRun()<CR>
    func! CompileRun()
        exec "w"
        if &filetype == 'python'
            exec "!time python3 %"
        endif
    endfunc
    ```

## 基础配置项

1. `set nu` -- 显示行号
2. `set hlsearch` -- 高亮显示搜索内容
3. `syntax on` -- 语法高亮显示
4. `colorscheme desert` -- 主题
5. `set autoindent` -- 换行保持当前缩进
6. `set ts=4` -- 一个tab键为4个空格
7. `filetype on` -- 打开文件类型检测
8. `set ignorecase` -- 搜索时不区分大小写
9. `set showmatch` -- 高亮显示匹配的括号
10. `set cursorline` -- 高亮当前光标所在行
11. `set noswapfile` -- 不产生`.swp`文件