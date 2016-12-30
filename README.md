# fancy-vim
定制属于你自己的Vim - 没有做不到的功能，只有你想不到的Vim   

**跟着大神学vim** [所需即所获：像 IDE 一样使用 vim](https://github.com/yangyangwithgnu/use_vim_as_ide)

## Elementary knowledge

**注释** `"` 单个双引号为注释标记    

**插件分类** vim插件分为`*.vim` `*.vba`, **前者** 是传统格式的文本文件，通常`someplugin.vim`(插件脚本) + `someplugin.txt`(帮助文档) 打包到一个文件中，解压后`someplugin.vim` 拷贝到 `~/.vim/plugin/` 目录,`someplugin.txt` 拷贝到 `~/.vim/doc/` 目录并`重启`即可；
但帮助文件需执行 `:helptags ~/.vim/doc/` 才能生效，可通过 `:h someplugin` 查看插件帮助信息。 **后者** 通过命令安装,like so:

```shell
vim someplugin.vba
:so %
:q
```

**插件管理工具** `vundle`

**`.vimrc`** vim配置文件,位于`~/.vimrc`,可以设置软链到其他目录下...

**`~/.vim/`** .vim/目录是存放插件的地方...

## Install & Configuration

### Upgrade vim

*make* 编译和安装项目的命令

*由于预安装的vim很多功能没有，so upgrade it,important！！！* 

**Config on Mac** Mac 默认支持很多语言如ruby python,我按照原文安装 **not work** so:

```shell
brew install vim --override-system-vi
```

### Install vundle

**清空`.vim/`** 目录

```shell
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

### Config .vimrc

省略查看`.vimrc`文件

#### Enter vim mode & Install Plugins

<img src="./vim.png"/>

```shell
vim

:PluginInstall
```

#### Remove Plugins

在`.vimrc`文件中注释或删除插件信息,and then:

```shell
vim

:PluginClean
```

#### Upgrade Plugins

**批量更新**
```shell
vim

:PluginUpdate
```

### Reference

[Vim常用命令](http://www.cnblogs.com/softwaretesting/archive/2011/07/12/2104435.html)    
[vim map nmap](http://www.cnblogs.com/lq0729/archive/2011/12/24/2300189.html)   
