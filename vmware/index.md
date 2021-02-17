# CODE


## Vmware
**tutorial**
[Catlin Wu youtube](https://www.youtube.com/c/CatlinWu/videos)

**WorkStation虚拟机迁移到 ESXi**
WorkStation虚拟机多个磁盘文件合并成一个
```
"C:\Program Files (x86)\VMware\VMware Player\vmware-vdiskmanager.exe" -r "d:\VMLinux\vmdkname.vmdk" -t 0 MyNewImage.vmdk
```
ssh登陆到vSphere
```
cd
/vmfs/volumes/51dc3538-bbdf69dc-6e61-782bcb765b0f/虚拟机文件夹/
vmkfstools -i 原文件名.vmdk 转换后文件名.vmdk -d thin
```

**update**
https://www.vediotalk.com/archives/3956

Download patches https://my.vmware.com/group/vmware/patch#search	
升级包上传
开启ESXI的SSH功能
```
vmware -vl
esxcli software sources profile list -d /vmfs/volumes/datastore1/VMware-ESXi-7.0U1c-17325551-depot.zip
esxcli software profile update -d  /vmfs/volumes/datastore1/VMware-ESXi-7.0U1c-17325551-depot.zip -p ESXi-7.0U1c-17325551-standard
reboot
```
> ESXi 7.0 后多出VMFS-L的空间如何删除VMFSL

引导后，按Shift+O键
autoPartitionOSDataSize=8192
注意大小写，回车安装即可。
