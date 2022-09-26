## Basic Operations for Starting Using a New Ubuntu System

### preliminary

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

### Git 操作

**设置用户信息**

* `git config --global user.name ""`
* `git config --global user.email ""`

**查看用户信息**

* `git config user.name`
* `git config user.email`

**设置记住密码**

`git config credential.helper store`

**git 常见操作**

* `git clone xxx`
* `git add/reset xxx`
* `git commit -m ""`
* `git push`
* `git config --global --unset http.proxy`

### Vim 操作

**`.vimrc`配置文件**

**安装插件**

### Jekyll + Github

参考[Design Homepage](https://rayh-ter.github.io/2022/09/26/design-homepage)
