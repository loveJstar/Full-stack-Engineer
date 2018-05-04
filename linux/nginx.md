## linux下搭建nginx代理

1. 安装nginx

		//一键安装上面四个依赖
		yum -y install gcc zlib zlib-devel pcre-devel openssl openssl-devel

2. 下载nginx的tar包

		//创建一个文件夹
		cd /usr/local
		mkdir nginx
		cd nginx
		//下载tar包
		wget http://nginx.org/download/nginx-1.13.7.tar.gz
		tar -xvf nginx-1.13.7.tar.g

	注：可以在官网直接下载然后通过ftp软件上传到linux服务器

3. 安装nginx

		//进入nginx目录
		cd /usr/local/nginx
		//执行命令
		./configure
		//执行make命令
		make
		//执行make install命令
		make install.

4. Nginx常用命令

		//测试配置文件
		安装路径下的/nginx/sbin/nginx -t
		//启动命令
		安装路径下的/nginx/sbin/nginx
		//停止命令
		安装路径下的/nginx/sbin/nginx -s stop
		或者 : nginx -s quit
		//重启命令
		安装路径下的/nginx/sbin/nginx -s reload

		//查看进程命令
		ps -ef | grep nginx
		//平滑重启
		kill -HUP Nginx主进程号

5. 开放端口

		//打开防火墙文件
		/etc/sysconfig/iptables
		/添加以下配置
		-A IN_public_allow -p tcp -m tcp --dport 80 -m conntrack --ctstate NEW -j ACCEPT
		重启防火墙
		service iptables restart