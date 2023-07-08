# pyocd_GUI简介

这是一个用于已经安装的pyocd的GUI界面，用于使用DAP-Link下载到单片机和生成命令，省去自己写命令的麻烦

# 用什么写的

[aardio](https://aardio.com/) ,为什么用这个？编写打包简单。

# 怎么使用

首先你得已经安装了[pyocd](https://github.com/pyocd/pyOCD)，因为这是只是一个GUI界面，只是通过生成命令后调用pyocd执行,然后直接打开这个就好啦

![一个图片](http://c.51hei.com/d/forum/202304/25/142034iz7zt6ovv44xttoo.png)

所见即所得，不用说明什么啦

# 问题

执行的时候不会显示跑进度条，执行结束才会刷新结果。我不知道怎么在aardio实现把命令行的进度条传出来，先凑合用。

# 怎么编译修改

下载aardio后直接打开工程文件（后缀为.aproj）点生成就行，啥也不用配置
