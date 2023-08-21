# pyocd_GUI简介

这是一个用于已经安装的pyocd的GUI界面，用于使用DAP-Link下载到单片机和生成命令，省去自己写命令的麻烦

# 用什么写的

[aardio](https://aardio.com/) ,为什么用这个？编写打包简单。

# 怎么使用

首先你得已经安装了[pyocd](https://github.com/pyocd/pyOCD)，因为这是只是一个GUI界面，只是通过生成命令后调用pyocd执行,然后直接打开这个就好啦

![一个图片](http://c.51hei.com/d/forum/202304/25/142034iz7zt6ovv44xttoo.png)

刷新列表可以安装全部已经安装支持的单片机，填写型号可以自动匹配，不用手工一个一个翻。

已经打包的应用位于目录下dist内，单文件直接复制出来就行。

# 问题

执行的时候不会显示跑进度条，执行结束才会刷新结果。我不知道怎么在aardio实现把命令行的进度条传出来，所以我直接~~在按键上显示了，用来反馈你已经按下了。~~显示一个提示框。

哦对了，在某个版本的jlink安装后（例如7.22），如果有使用hid的Daplink，会导致生成一个sergger 第三方dap（Segger 3rd party CMSIS-DAP），不要选那个，为了能方便查看我没做过滤，只会自动不首选，实际上这个需要调用jlink而且兼容性不好。

为了提高打开速度，所以默认型号是手工写进去的，有需要可以自行修改为打开之后自动刷新列表，或者改成自己常用的。

# 怎么编译修改

## 编译
由于我用到了得意黑字体，所以需要安装这个字体到系统，然后下载aardio后直接打开工程文件（后缀为.aproj）点发布就行，其他的啥也不用配置。如果你不喜欢这个字体，去掉对这个字体的包含并修改用到了这个字体的控件所用字体即可。
## 修改
看aardio的教程吧，就。。挺朴素的？
