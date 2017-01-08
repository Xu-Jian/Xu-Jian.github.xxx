---
layout: post
title: Find - Kali/Debian
tags: Misc
categories: 👓
---


## Find - Kali/Debian

`find` + `搜索路径` + 语法(文件名关键字) 

路径:  `/`   `~`  `.`(当前目录下)


**-name**   
`-name `  大小写敏感
`-iname` 大小写不敏感

 
- `find ~ -name itr.txt`
	> home目录下找文件

- `find . -name itr.txt`
	> 当前目录下寻找

- `find . -name “[A-Z]*”`
	> 找 一个大写字母开头文件.

- `find / -name "*"`
	> 让系统高负荷运行!!!   
	> 从根目录开始查找所有文件.

- `find /etc -name "host"`
	> /etc 中查找 host 开头文件.



**-perm**
按照权限模式查找:

- `find . -perm 755`
	找出当前目录下 权限是755的文件.

	- `find . -perm 777`
		找出当前目录下 权限是777的文件 


		 
如:home 目录下 找 `*.log`




**mtime,atime,ctime**
安装 文件 修改时间 找

`-` -5 表示5天内
`+` +5 表示5天前









       which  查看可执行文件的位置。
       whereis 查看文件的位置。 
       locate   配合数据库查看文件位置。
       find   实际搜寻硬盘查询文件名称。
which命令的作用是，在PATH变量指定的路径中，搜索某个系统命令的位置，并且返回第一个搜索结果。也就是说，使用which命令，就可以看到某个系统命令是否存在，以及执行的到底是哪一个位置的命令。 
1．命令格式：
which 可执行文件名称 
2．命令功能：
which指令会在PATH变量指定的路径中，搜索某个系统命令的位置，并且返回第一个搜索结果。
3．命令参数：
-n 　指定文件名长度，指定的长度必须大于或等于所有文件中最长的文件名。
-p 　与-n参数相同，但此处的包括了文件的路径。
-w 　指定输出时栏位的宽度。
-V 　显示版本信息
4．使用实例：
实例1：查找文件、显示命令路径
命令：
which lsmod
 
 
用 which 去找出 which
命令：
  which which
 
 
找出 cd 这个命令
命令：
 which cd
 
 