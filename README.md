需要安装`linux-headers`, 然后执行:
```
$cd ./src
$make
#make install
```
会在```/lib/modules/`uname -r`/kernel/net/netfilter/ipvs/```目录生成`toa.ko`文件。
手动`modprobe toa`完成加载。


如果需要支持重启后自动加载模块，在`/etc/modprobe.d/`或者`/etc/modules-load.d/`目录新建一个`081-toa.conf`文件，
单独一行写入`toa`即可。

