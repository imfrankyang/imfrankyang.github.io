# Vmware



### Tutorial  
[Catlin Wu youtube](https://www.youtube.com/c/CatlinWu/videos)



### VMware Workstation to ESXi  

1. WorkStation虚拟机多个磁盘文件合并成一个

```shell
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -r "d:\VMLinux\vmdkname.vmdk" -t 0 vmdknamenew.vmdk
```
2. ssh登陆到vSphere
```bash
cd /vmfs/volumes/虚拟机文件夹/
vmkfstools -i 原文件名.vmdk 转换后文件名.vmdk -d thin
```

### ESXi update

https://www.vediotalk.com/archives/3956

1. Download patches https://my.vmware.com/group/vmware/patch#search	
2. 升级包上传
3. 开启ESXI的SSH功能
4. ssh 输入
```bash
vmware -vl
esxcli software sources profile list -d /vmfs/volumes/datastore1/VMware-ESXi-7.0U1c-17325551-depot.zip
esxcli software profile update -d  /vmfs/volumes/datastore1/VMware-ESXi-7.0U1c-17325551-depot.zip -p ESXi-7.0U1c-17325551-standard
reboot
```


### VMware Workstation to Virtualbox**

```shell
"C:\Program Files (x86)\VMware\VMware Workstation\OVFTool\ovftool.exe" "D:\vmware.vmx"  "D:\vmware.ovf"
```


### VMware Workstation 安装macos

下载[com.vmware.fusion.zip.tar](https://softwareupdate.vmware.com/cds/vmw-desktop/fusion/12.1.0/17195230/core/com.vmware.fusion.zip.tar)，放到unlocker/tools/


### VMware Workstation 硬盘操作

**压缩硬盘**
```bash
#mac虚拟机内
cat /dev/zero > wipefile; rm wipefile
sudo /Library/Application\ Support/VMware\ Tools/vmware-tools-cli disk shrink /

#win主系统 
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -k "D:\vmware.vmdk" 

#linux虚拟内
sudo rm -rf .cache/
sudo /usr/bin/vmware-toolbox-cmd disk list
sudo vmware-toolbox-cmd disk shrink /
```

**重命名vmdk文件**
```shell
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -n "source.vmdk" "target.vmdk"
```

**合并硬盘**
```shell
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -r "C:\vmware1.vmdk" -t 0 "C:\vmware2.vmdk"
```

**分割硬盘**
```shell
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -r "C:\vmware1.vmdk" -t 1 "C:\vmware2.vmdk"
```

-r参数指定源磁盘文件  
-t参数指定输出虚拟磁盘文件的类型，其值为以下类型之一：  
0：创建一个包含在单一虚拟文件中的可增长虚拟磁盘  
1：创建一个被分割为每个文件2GB大小的可增长虚拟磁盘  
2：创建一个包含在单一虚拟文件中的预分配虚拟磁盘  
3：创建一个被分割为每个文件2GB大小的预分配虚拟磁盘  

**vmware 扩大硬盘**
1. add a new virtual disk
2. clone disk
```
   dd if=/dev/sdb  of=/dev/sdc
```
3. remove the old virtual disk and start
4. there is a error: the root filesystem requires a manual fsck 
```
fsck -yf /dev/sda1
```
5. resize disk in disk app   

### vmware tools
It seems that the vmware official recommend the `open vm tools`.
```
#install
sudo ./vmware-tools-distrib/vmware-install.pl

#uninstall
sudo ./vmware-tools-distrib/bin/vmware-uninstall-tools.pl
```

{{< admonition tip "" true >}}
当再次安装Vmware Tools出现错误。
{{< /admonition >}}

安装前把 /usr/lib/vmware-tools删除： rm -rvf /usr/lib/vmware-tools


### open vm tools
- https://github.com/vmware/open-vm-tools  
- https://docs.vmware.com/cn/VMware-Tools/11.0.0/com.vmware.vsphere.vmwaretools.doc/GUID-C48E1F14-240D-4DD1-8D4C-25B6EBE4BB0F.html  

**install**
```bash
#ubuntu
sudo apt install open-vm-tools
sudo apt install open-vm-tools-desktop
sudo apt install xorg-x11-drv-vmware

#centos
sudo yum install open-vm-tools
sudo yum install open-vm-tools-desktop
sudo yum install xorg-x11-drv-vmware
```

**uninstall**
```bash
#ubuntu
apt remove open-vm-tools-desktop

#centos8
dnf remove open-vm-tools
```




### 常见问题
{{< admonition tip "" true >}}
安装ESXi 7.0 后多出VMFS-L的空间如何删除VMFSL
{{< /admonition >}}
u盘引导后，按Shift+O键  
autoPartitionOSDataSize=8192  
注意大小写，回车安装即可。  


{{< admonition tip ""  true >}}
网卡无法启动的解决方法
{{< /admonition >}}

1. 虚拟机设置里删除旧网卡，重新添加网卡
2. ifconfig ens33 up
3. /sbin/dhclient

如果设置里面network没有网络信息，输入：
```bash
sudo service network-manager stop
sudo rm /var/lib/NetworkManager/NetworkManager.state
sudo vim /etc/NetworkManager/NetworkManager.conf 
sudo service network-manager restart
```
备用方法
```bash
系统自带的NetworkManager这个管理套件影响到网卡的启动，关掉就可以解决
systemctl stop NetworkManager       # 停止NetworkManager
systemctl disable NetworkManager    # 并使其失效，开机不启动
systemctl start network             # 启动网络后就OK了
```


{{< admonition tip ""  true >}}
linux虚拟机缩放
{{< /admonition >}}

```
sudo yum install xorg-x11-drv-vmware
```
备用方法
```bash
xrandr --output Virtual1 --scale 0.9x0.9
xrandr --output Virtual1 --scale 1x1
xrandr --output Virtual1 --scale 0.4x0.4
```





