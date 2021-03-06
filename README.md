# Linux-ubuntu
This my remark.

### 1.lenovo can not use wifi in ubuntu system
<pre>sudo modprobe -r ideapad_laptop</pre>

### 2.how to install go on linux
<pre>export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GOBIN=$GOPATH/bin
export PATH=$GOROOT/bin:$PATH:$GOBIN
</pre>

### 3.install unity tweak tool

### 4.how to install Linux [link](https://www.jianshu.com/p/123489c8b991)

### 5.modify environmental variable
<pre> sudo gedit ~/.bashrc 
 after modifying, source ~/.bashrc</pre>
 
### 6. How to install shadowsocks?
[Tutorial](https://github.com/Billy1900/AWS-Shadowsocks)
change the `auto switch` mode in switchOmega sometimes when you can not connect with google.


### 7. 硬盘分区

在Linux系统中每一个硬盘总共最多有 16个分区，硬盘上的4个主分区，分别标识为sdal、sda2、sda3和sda4，逻辑分区则从sda5开始标识一直到sda16

Ubuntu Linux可以把分区作为挂载点，载入目录，其中最常用的硬盘大小（500G-1000G）分配目录推荐如下表所示：

|目录|	建议大小|	格式| 描述|
|----|-----|----|-----|
|/	|150G-200G	|ext4	|根目录|
|/swap	|物理内存两倍|	swap|	交换空间：交换分区相当于Windows中的“虚拟内存”，如果内存低的话（1-4G），物理内存的两倍，高点的话（8-16G）要么等于物理内存，要么物理内存+2g左右，|
|/boot	|1G左右	|ext4|	空间起始位置 分区格式为ext4 /boot  </br>建议：应该大于400MB或1GB Linux的内核及引导系统程序所需要的文件，比如 vmlinuz initrd.img文件都位于这个目录中。在一般情况下，GRUB或LILO系统引导管理器也位于这个目录；启动撞在文件存放位置，如kernels，initrd，grub。|
|/tmp	|5G左右	|ext4	|系统的临时文件，一般系统重启不会被保存。（建立服务器需要？）|
|/home	|尽量大些	|ext4|	用户工作目录；个人配置文件，如个人环境变量等；所有账号分配一个工作目录|

### 8. minimize dock
`gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'`


### 9. Linux目录结构

![image](https://github.com/Billy1900/Linux-ubuntu/blob/master/Untitled%20picture.png)

Linux 文件系统是一个目录树的结构，文件系统结构从一个根目录开始，根目录下可以有任意多个文件和子目录，子目录中又可以有任意多个文件和子目录
- bin 存放二进制可执行文件(ls,cat,mkdir等)
- boot 存放用于系统引导时使用的各种文件
- dev 用于存放设备文件
- etc 存放系统配置文件
- home 存放所有用户文件的根目录
- lib 存放跟文件系统中的程序运行所需要的共享库及内核模块
- mnt 系统管理员安装临时文件系统的安装点
- opt 额外安装的可选应用程序包所放置的位置
- proc 虚拟文件系统，存放当前内存的映射
- root 超级用户目录
- sbin 存放二进制可执行文件，只有root才能访问
- tmp 用于存放各种临时文件
- usr 用于存放系统应用程序，比较重要的目录/usr/local 本地管理员软件安装目录
- var 用于存放运行时需要改变数据的文件


### 10. [Ubuntu/Win10双系统安全删除Ubuntu的方法](https://blog.csdn.net/Meditator_hkx/article/details/52626077)

### 11. [Windows + Ubuntu 16.04 双系统安装详细教程](https://blog.csdn.net/flyyufenfei/article/details/79187656)

### 12. [Linux连接锐捷校园网客户端](https://blog.csdn.net/qq_15015129/article/details/52651303)

### 13. [VMware 虚拟机无法连接网络解决办法](https://blog.csdn.net/m0_37259197/article/details/78221016)

### 14. [Linux内核版本介绍与查询](https://jasonhzy.github.io/2019/02/05/linux-kernel-version/)

### 15. [Ubuntu 18.04 安装 NVIDIA 显卡驱动](https://zhuanlan.zhihu.com/p/59618999)

### 16. [E: Unmet dependencies. Try 'apt --fix-broken install' with no packages (or specify a solution)](https://unix.stackexchange.com/questions/476059/e-unmet-dependencies-try-apt-fix-broken-install-with-no-packages-or-speci)

### 17. [虚拟机如何让屏幕自适应客户机窗口大小](https://blog.csdn.net/lipeng19930407/article/details/80955322)
sudo apt-get install open-vm-tools

### 18. How to make a free server for you to look through foreign websites like Google?
**18.1 Tutorial**
- [The tutorial](http://dongdongdong.me/2018/01/31/OS/Installation/Ubuntu/ladder/)
- [How to install shadowsocks on ubuntu](https://zhuanlan.zhihu.com/p/47706985)
- [how to use proxy on linux:chrome,firefox](https://www.dev2qa.com/how-to-setup-shadowsocks-vpn-on-mac-windows-and-linux/)
- [How to Set up Shadowsocks-libev Proxy Server on Ubuntu 16.04/17.10](https://www.linuxbabe.com/ubuntu/shadowsocks-libev-proxy-server-ubuntu-16-04-17-10)
- [How to remove shadowsocks from Ubuntu 16.04 (Xenial Xerus)](https://www.howtoinstall.co/en/ubuntu/xenial/shadowsocks?action=remove)
- [视频教程](https://www.youtube.com/watch?v=nQoIazBEU8I)

**18.2. Q&A**
- putty
<pre>
sudo su
apt-get update
apt-get upgrade
apt-get install python-pip
pip install shadowsocks
pip install m2crypto
vim /etc/shadowsocks.json
ssserver -c /etc/shadowsocks.json -d start
<pre>
{     
"server":"0.0.0.0",     
"server_port":443,     
"local_address": "127.0.0.1",     
"local_port":1080,     
"password":"mypassword",     
"timeout":300,     
"method":"aes-256-cfb",     
"fast_open": false,     
"workers": 1 
}
</pre>
vim /usr/local/lib/python2.7/dist-packages/shadowsocks/crypto/openssl.py     `cleanup`  ->   `reset`
本地配置shadowsocks
开机启动：vi /etc/rc.local
   写入 <code>ssserver -c /etc/shadowsocks.json
      exit 0</code>
 在root下运行：chown root:root /etc/rc.local
       chmod 755 /etc/rc.local
       systemctl enable rc-local.service
  最后再reboot
</pre>

**18.2 测试网站**
- [ping 测速](http://ping.chinaz.com)
- [连接不上](https://blog.csdn.net/daerzei/article/details/81169349)

**18.3 notice**
大陆用户选择Seoul or Tokyo

[如何选择节点位置？](https://www.cloudping.info)
