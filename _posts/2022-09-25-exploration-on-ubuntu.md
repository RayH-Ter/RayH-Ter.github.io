---
title: Exploration on Ubuntu
author: raymond
date: 2022-09-25 16:34:00 +0800
category: [Linux, Basis]
tags: [Ubuntu, Introduction]
---

## Basic Operations For A New Ubuntu System

### Preliminary

**安装与卸载**

```powershell
wsl --list
wsl --unregister Ubuntu
```

**更改密码**

```bash
sudo passwd update
su
```

**添加代理**

1. `cat /etc/resolv.conf`查看IP地址，记作yourip
2. 查看代理窗口（如Clash客户端界面），记作yourport
3. 进入WSL Ubuntu，执行`export ALL_PROXY="http://yourip:yourport"`
4. 当主机ip发生变化时需重新设置

**换源**

需要保证源的正确性：

1. 通过`lsb_release -a`查看Ubuntu版本
2. 参考网址：[sunanli](https://www.cnblogs.com/sunanli/p/13797042.html) 复制源，更改`/etc/apt/sources.list`文件
3. `sudo apt-get update`

**安装软件**

1. `sudo apt install vim`
2. `sudo apt install build-essential`
3. `sudo apt install valgrind`

**更改文件/目录权限**

* `chown`命令，详见[wuling129](https://www.cnblogs.com/wuling129/p/4648760.html)

**wsl与windows文件相互访问**

* wsl访问windows文件：`/mnt/`目录下即为windows磁盘
* windows访问wsl文件：文件管理器左侧显示的`Linux`即为wsl

### Git 操作

**设置用户信息**

`git config --global user.name ""` \
`git config --global user.email ""`

**查看用户信息**

`git config user.name`\
`git config user.email`

**设置记住密码**

`git config credential.helper store`

**常见操作**

`git clone xxx` \
`git add/reset xxx` \
`git commit -m ""` \
`git push` \
`git config --global --unset http.proxy`

### Vim 操作

`sudo apt-get install vim`

**`.vimrc`配置文件**

1. `vim ~/.vimrc` open the config file
2. install Vundle and use it to install plugs you'd like to use.
    1. `git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
    2. edit your .vimrc file and put your plug installation statement between `call vundle#begin()` and `call vundle#end()`. Just do it as follows:
        ```vim
        call vundle#begin()
        " default installation
        Plugin 'VundleVim/Vundle.vim'
        " install doxygen for better comments, usage like, :Dox, :DoxAuthor
        Plugin 'vim-scripts/DoxygenToolkit.vim'
        " install Chinese vim document, usage like, :help
        Plugin 'asins/vimcdoc'
        call vundle#end()
        ```
        then, save the file and use `:PluginInstall` to start installation.

> https://vimcdoc.sourceforge.net/

**安装插件**

### Jekyll + Github

> 参考[Design Homepage](https://rayh-ter.github.io/2022/09/26/design-homepage)
