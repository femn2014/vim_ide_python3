# vim_ide_python3 vim_grammar
1.Vundle管理vim的插件

	git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim

2.vim编辑markdown时实现预览功能

安装vim-instant-markdown,当打开.md文件时会被Nodejs直接运行，预览到浏览器中，安装完成后，
只要vim打开了markdown类型的文件就会自动打开一个浏览器窗口实时预览

	vim-instant-markdown安装之前需要：
	sudo add-apt-repository ppa:chris-lea/node.js
	sudo apt-get update  # 则会有下面的sources
	vim /etc/apt/sources.list.d/chris-lea-ubuntu-node_js-xenial.list
		deb http://ppa.launchpad.net/chris-lea/node.js/ubuntu xenial main  
	sudo apt-get install nodejs
	sudo apt-get install npm
	sudo npm -g install instant-markdown-d

3.vim 配置成Python IDE 

    sudo apt-get install curl vim exuberant-ctags git ack-grep
    sudo pip install pep8 flake8 pyflakes isort yapf
     

4.安装插件

    curl -o .vimrc https://file.femnyy.com/file/.vimrc
    mv .vimrc ~/.vimrc
    sudo vim 
    :PlugInstall 

此时的~/.vim/目录下就已经安装好所有的插件了.

5.安装和运行ctage

	sudo apt-get install exuberant-ctags
    # 手动创建索引
	cd ~/app1.6
	ctags -R *
	# 应该可以用!cd /home/python/app1.6 && ctags -R *
	# Linux下的C/C++的程序员，使用VIM+Ctags的组合来写程序也许是最佳的选择
    # 好像没有递归子目录，所以为子目录创建索引
    cd main && ctags -R *
    cd ../app1.6 #必须要cd到此目录或者 main目录下，可由 :set tags 查看
    vim runner
    # 这样本地的所有代码，都正确的创建了索引,但源代码还是没有办法创建索引

6.增加自动折叠功能
    
    zo 展开
    zc 收到
    zn 全部展开
    zN 全部折叠

7.一些基本操作

    F2 # 将本行快速居中
    F3 # 打开左侧的文件树,相当于是分割窗口了,<ctrl-w>w进行转换
    F4 # 在右侧显示所有的方法
    <ctrl-6> # 在两个文件中快速切换
    [N]<ctrl-w>< # > # 改变窗口的宽度

### 注意不能复制剪贴板的内容
