
# `zsh-autosuggestions`自动补全插件的安装和使用

1. 下载该插件到`.oh-my-zsh`的插件目录

    ```
        git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
    ```

2. 编辑`.zshrc`文件

    找到`plugins=(git)`这一行，如果没有添加。在括号中添加`zsh-autosuggestions`
    
    ```
        plugins=(git zsh-autosuggestions)
    ```

3. 重启命令

***

# `incr`也是自动补全插件

1. 下载自动补全插件`http://mimosa-pudica.net/src/incr-0.2.zsh`

2. 放到`oh-my-zsh`的插件库中    

    `.oh-my-zsh/plugins/`创建`incr`文件夹放到该文件夹中

3. 在`.zshrc`中添加   
    
    在`.zshrc`文件末尾添加下面这行

    `source ~/.oh-my-zsh/plugins/incr/incr*.zsh`

4. 重启命令行
