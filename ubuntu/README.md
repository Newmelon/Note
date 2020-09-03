# SSH远程服务

### 1.安装：

```
sudo apt-get install openssh-server
```

### 2.开机自启：

```
sudo systemctl enable ssh
```

### 3.重启：

```
reboot
```

# 永久挂载硬盘

### 1.创建文件夹及改权限：

```
cd /
mkdir data1
sudo chmod 777 data1
```

### 2.查看已挂载分区：

```
df -h
```

### 3.查看磁盘信息：

```
fdisk -l
```

### 4.挂载磁盘：

```
mount /dev/sdb  /data1
```

### 5.永久挂载：

```
vim /etc/fstab
```

#### 	添加下面两行：

/dev/sdb /data1 ext4 defaults 0  0

/dev/sdc /data2 ext4 defaults 0  0

### 6.重启：

```
reboot
```

