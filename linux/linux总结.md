# 1. 使用资源 #
	1. 自我购买的网上课程：
	[http://www.ydma.com/classroom/14/task](http://www.ydma.com/classroom/14/task)


# 2. 学习总结 #

	## 1.基本操作 ##
		r:cat,more,head,tail,ls
		w:vim,echo,touch,rm,mv,cp
		x:cd,find,whereis,grep,ln -s

----------

	## 2.管理 ##
		权限:r-w-x(4-2-1),777,chmod,chown,chgrp
		用户:useradd,groupadd,passwd,userdel,groupdel
		启动:shutdown,reboot,init 6
		进程:ps aux,top,kill -9
		磁盘:su/df/du

----------

	## 3.计划任务 ##
		*（分钟）*（时）*（日）*（月）*（周）
		10   9 1 1 *   ：表示，1月1日9点10分执行
		*/10 * * * 1-3 :表示，周一到周三每隔10分钟执行

----------

	## 4.实践 ##
		yum -y install/update/remove
		tar -zcvf
		tar -zxvf
		源码包安装：1.tar -zxvf 2.cd 到文件中；3.查看readme;4.配置路径：./configure--prefix=/usr/local/路径；5.make & make install



# 3. 遇到问题汇总 #

	1. linux 忘记密码的处理方法[https://wenku.baidu.com/view/35f29600a6c30c2259019eeb.html](https://wenku.baidu.com/view/35f29600a6c30c2259019eeb.html)
	

----------

	2. linux下安装apache常见的错误
	[https://www.cnblogs.com/zlxdbokeyuan/p/5022439.html](https://www.cnblogs.com/zlxdbokeyuan/p/5022439.html)

----------

	3. linux下查看系统版本（cat /etc/issue）
	[http://www.ha97.com/2987.html](http://www.ha97.com/2987.html)

----------

	4. 安装apache过程中，遇到的问题：relocation R_X86_64_32 against `.rodata' can not be used when making a shared object; recompile with -fPIC
	[http://www.cnblogs.com/bluewelkin/p/4323331.html](http://www.cnblogs.com/bluewelkin/p/4323331.html)

----------

	5. linux 添加环境变量的方法
	#export PATH=$PATH:路径
	[http://www.cnblogs.com/amboyna/archive/2008/03/08/1096024.html](http://www.cnblogs.com/amboyna/archive/2008/03/08/1096024.html)