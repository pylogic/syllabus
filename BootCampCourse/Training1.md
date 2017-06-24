# Training 1: Linux, Python and Git basics

Ganben

## 0 Desktop Env
windows用户建议安装Cygwin 和Git准备好桌面环境。

- [Cygwin](https://www.cygwin.com/) 是一个在Win桌面上模拟Linux OS操作工具，主要提供了SSH远程登录功能。它也可以运行大多数的linux命令和程序。在安装Cygwin时，请务必勾选ssh/sshd模块

- [Git](https://git-scm.com/downloads) 可以安装在Windows 命令行中，也可以安装在Cygwin中。在windows桌面下的安装可以有GUI版本。

## 1 Cloud server: LVM
####1.1 登陆服务器
测试和生产环境为LVM技术提供的云端服务器环境。使用ssh的username + password或者key方式认证。
根据分配的*username*和*password*，运行：

`` ssh username@IP``

如果需要使用密码登陆的，在提示符下输入密码后回车。（光标不会动的，不要管）


####1.2 服务器环境查看
- 尝试以下命令：`whoami`,`uname -a`, `w`

####1.3 APT 程序管理

- sudo apt list 
- sudo apt install *anyprogram*
- sudo apt update
- sudo apt upgrade
- sudo apt remove 

####1.4 PATH等环境变量

- echo $PATH
- export PATH=$PATH:*anypath*
- vi ~/.bashrc

####1.5 TOP

查看服务器CPU内存占用情况

####1.6 可选查看网络
查看网络端口，链接数，IP地址，防火墙设置

## 2 Python

####2.1 Python环境

- python -V 
- python3 -V
- pip list
- pip install virtualenv --trusted-host=http://pypi.douban.com/simple/
- import

## 3 GIT

####3.1 git config

- git config --global user.name " "
- git config --global user.email " "