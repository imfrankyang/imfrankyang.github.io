# Vmware



**tutorial**  
[Catlin Wu youtube](https://www.youtube.com/c/CatlinWu/videos)


**WorkStation to ESXi**  

1. WorkStation虚拟机多个磁盘文件合并成一个

```shell
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -r "d:\VMLinux\vmdkname.vmdk" -t 0 vmdknamenew.vmdk
```
2. ssh登陆到vSphere
```bash
cd /vmfs/volumes/虚拟机文件夹/
vmkfstools -i 原文件名.vmdk 转换后文件名.vmdk -d thin
```


**ESXi update**

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


**VMware to Virtualbox**

```shell
"C:\Program Files (x86)\VMware\VMware Workstation\OVFTool\ovftool.exe" "D:\vmware.vmx"  "D:\vmware.ovf"
```


**vmware安装macos**

下载[vmware tools](https://softwareupdate.vmware.com/cds/vmw-desktop/fusion/12.1.0/17195230/core/com.vmware.fusion.zip.tar)  
com.vmware.fusion.zip.tar放到unlocker/tools/


**vmware 压缩硬盘**

```bash
#mac 系统内
cat /dev/zero > wipefile; rm wipefile
sudo /Library/Application\ Support/VMware\ Tools/vmware-tools-cli disk shrink /

#win 
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -k "D:\vmware.vmdk" 

#linux 系统内
sudo rm -rf .cache/
sudo /usr/bin/vmware-toolbox-cmd disk list
sudo vmware-toolbox-cmd disk shrink /
```

```shell
#重命名vmdk文件
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -n "source.vmdk" "target.vmdk"

#合并硬盘
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -r "C:\vmware1.vmdk" -t 0 "C:\vmware2.vmdk"

#分割硬盘
"C:\Program Files (x86)\VMware\VMware Workstation\vmware-vdiskmanager.exe" -r "C:\vmware1.vmdk" -t 1 "C:\vmware2.vmdk"
```
-r参数指定源磁盘文件  
-t参数指定输出虚拟磁盘文件的类型，其值为以下类型之一：  
0：创建一个包含在单一虚拟文件中的可增长虚拟磁盘  
1：创建一个被分割为每个文件2GB大小的可增长虚拟磁盘  
2：创建一个包含在单一虚拟文件中的预分配虚拟磁盘  
3：创建一个被分割为每个文件2GB大小的预分配虚拟磁盘  



**open vm tools**  
https://github.com/vmware/open-vm-tools  
https://docs.vmware.com/cn/VMware-Tools/11.0.0/com.vmware.vsphere.vmwaretools.doc/GUID-C48E1F14-240D-4DD1-8D4C-25B6EBE4BB0F.html  

```bash
sudo apt install open-vm-tools
sudo apt install open-vm-tools-desktop
```



{{< admonition tip "" true >}}
ESXi 7.0 后多出VMFS-L的空间如何删除VMFSL

u盘引导后，按Shift+O键  
autoPartitionOSDataSize=8192  
注意大小写，回车安装即可。  
{{< /admonition >}}



{{< admonition tip ""  true >}}
网卡无法启动的解决方法

```bash
系统自带的NetworkManager这个管理套件影响到网卡的启动，关掉就可以解决
systemctl stop NetworkManager	#停止NetworkManager
systemctl disable NetworkManager	#并使其失效，开机不启动
systemctl start network		#启动网络后就OK了
```
{{< /admonition >}}



{{< admonition tip ""  true >}}
linux虚拟机缩放

```bash
xrandr --output Virtual1 --scale 0.9x0.9
xrandr --output Virtual1 --scale 1x1
xrandr --output Virtual1 --scale 0.4x0.4
```
{{< /admonition >}}




