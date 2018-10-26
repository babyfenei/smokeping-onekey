# SmokePing一键管理脚本 #


## 更新内容 ##
1.本脚本通过https://github.com/ILLKX/smokeping-onekey修改而来，在原作的基础上添加了邮件报警，
2.邮件报警的同时会对目标主机进行ping测和MTR测试。
3.脚本添加nali数据库，在ping测和MTR的同时对IP进行归属解析。
4.脚本修改配置文件，将所有的检测节点添加到targets配置文件中，如需添加节点只需要修改此文件即可。
5.如需开机启动，可将此命令添加至/etc/rc.local中```echo '7' | bash /root/smokeping-onekey/smokeping.sh --stdin```,请在实际使用中修改脚本存放路径

## 原版介绍 ##
一个Shell脚本，集成SmokePing三种版本(Master/Slaves/单机版)安装、启动、停止、重启等基本操作，方便用户操作。

[https://www.sabia.cc/smokeping-onekey.html](https://www.sabia.cc/smokeping-onekey.html)

## 系统支持 ## 
* CentOS 7
* CentOS 6 (有bug请反馈)

## 功能 ##
- 一键启动、停止、重启SmokePing服务
- 一键安装、卸载SmokePing三种版本
- 一键安装Tcpping (Smokeping专用版本)
- 自动更换阿里云源(可选)
- 支持中文显示
- 覆盖安装提醒

## 缺点 ##
- 未设置开机启动
- Master端/单机版会自动安装Nginx并修改Nginx默认配置

## 注意事项 ##
- 请尽量确保服务器环境干净，最好重新安装系统后使用此脚本
- 本脚本只为方便用户安装/管理SmokePing，请用户自行配置SmokePing
- 每次修改SmokePing配置文件后请重启SmokePing
- 此脚本安装的Tcppinng仅适用于SmokePing

## 安装/卸载 ##
    wget -N --no-check-certificate https://raw.githubusercontent.com/ILLKX/smokeping-onekey/master/smokeping.sh && bash smokeping.sh

## 截图 ##
![https://raw.githubusercontent.com/ILLKX/smokeping-onekey/master/1.jpg](1.jpg)

![https://raw.githubusercontent.com/ILLKX/smokeping-onekey/master/2.jpg](2.jpg)

## 参考资料 ##
[CentOS7详细安装配置SmokePing教程-来自lala.im](https://lala.im/2821.html)

[SmokePing主从服务器详细配置教程-来自lala.im](https://lala.im/2867.html)

[参考逗比的mt-proxy安装脚本部分代码](https://github.com/ToyoDAdoubi/doubi)

[Tcpping-SmokePing](https://github.com/tobbez/tcpping-smokeping)
