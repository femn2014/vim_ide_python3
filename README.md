[1. install Docker](http://wiki.jikexueyuan.com/project/docker/installation/debian.html)

[本人一些有关docker的学习](https://www.femnyy.com/docker/)

2. 设置一个简单的别名

    alias vim-python='docker run -it --rm -v $(pwd):/src femn/vim_python'

3.运行

    vim-python # 需要下载镜像，可能会比较慢
    # 打开的vim的文件管理系统，选择需要编辑的文件既可
    # 编辑时 会在容器的/src/下编辑，保存退出之后，会保存到主机的$(PWD)目录下
