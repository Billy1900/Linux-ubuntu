# Linux-ubuntu
Some remarks


1.lenovo can not use wifi in ubuntu system
 <pre>sudo modprobe -r ideapad_laptop</pre>

2.how to install go on linux
<pre>export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GOBIN=$GOPATH/bin
export PATH=$GOROOT/bin:$PATH:$GOBIN
</pre>

3.install unity tweak tool

4.how to install linux

5.modify environmental variable
<pre> sudo gedit .bashrc 
 after modifying, source .bashrc</pre>
 
6. How to install shadowsocks?

[Tutorial](https://github.com/Billy1900/AWS-Shadowsocks)
change the `auto switch` mode in switchOmega sometimes when you can not connect with google.


7. 硬盘分区

在Linux系统中每一个硬盘总共最多有 16个分区，硬盘上的4个主分区，分别标识为sdal、sda2、sda3和sda4，逻辑分区则从sda5开始标识一直到sda16

Ubuntu Linux可以把分区作为挂载点，载入目录，其中最常用的硬盘大小（500G-1000G）分配目录推荐如下表所示：

|目录|	建议大小|	格式| 描述|
|----|-----|----|-----|
|/	|150G-200G	|ext4	|根目录|
|/swap	|物理内存两倍|	swap|	交换空间：交换分区相当于Windows中的“虚拟内存”，如果内存低的话（1-4G），物理内存的两倍，高点的话（8-16G）要么等于物理内存，要么物理内存+2g左右，|
|/boot	|1G左右	|ext4|	空间起始位置 分区格式为ext4 /boot  </br>建议：应该大于400MB或1GB Linux的内核及引导系统程序所需要的文件，比如 vmlinuz initrd.img文件都位于这个目录中。在一般情况下，GRUB或LILO系统引导管理器也位于这个目录；启动撞在文件存放位置，如kernels，initrd，grub。|
|/tmp	|5G左右	|ext4	|系统的临时文件，一般系统重启不会被保存。（建立服务器需要？）|
|/home	|尽量大些	|ext4|	用户工作目录；个人配置文件，如个人环境变量等；所有账号分配一个工作目录|


8. minimize dock
`gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'`
