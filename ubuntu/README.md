# SSH远程服务

安装：

```
sudo apt-get install openssh-server
```

开机自启：

```
sudo systemctl enable ssh
```

重启：

```
reboot
```

# 永久挂载硬盘

创建文件夹

```
mkdir path
```

查看已挂载分区

```
df -h
```

查看磁盘信息

```
fdisk -l
```

挂载磁盘

```
mount /dev/sdb  /data1
```

永久挂载

```
vim /etc/fstab
```

添加下面两行

/dev/sdb /data1 ext4 defaults 0  0

/dev/sdc /data2 ext4 defaults 0  0

