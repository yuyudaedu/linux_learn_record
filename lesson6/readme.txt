
	关于sshd服务端管理其它计算机的补充：
	
	配置后: service sshd restart
	登录其它计算机:  ssh root@192.168.0.1
	如果GSSAPIAuthentication yes 则就要通过DNS验证，会报一个warming的警告，而且非常之慢。如果没有DNS设为no.
	如果PermitRootLogin  no   就不能用root用户登录另外的计算机，但非root用户就能登录，(su命令切换可以进到root)保证了权限的控制。
	用ifconfig查看ip变成了另一台计算机的ip.
