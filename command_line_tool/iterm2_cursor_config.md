# iTerm2中移动光标的配置

命令行中默认的光标移动 

* `ctrl + a` : 移动到行首

* `ctrl + e` : 移动到行尾

* `esc + f` : 向前移动一个单词

* `esc + b` : 向后移动一个单词

修改为使用`ctrl + f/b`来移动光标

## 修改步骤如下

1. 进入iTerm2的偏好设置

2. 进入Profiles标签

3. 选择Keys

4. 点击添加

5. 添加自定义设置

	1. Keyboard Shortcut 输入 :ctrl + f 

	2. Action 选择Send Escasp Sequence

	3. 弹窗中会出现 `Esc + `的输入框，输入f 
