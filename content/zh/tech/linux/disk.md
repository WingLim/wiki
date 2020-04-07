---
title: "Linux 磁盘管理"
date: 2020-04-07T11:08:35+08:00
draft: true
---

## 查看文件系统空间信息

```bash
# -h: human-readable 
$ df -h
```

Example Result:

```bash
aegir@0xday:~$ df -h
Filesystem      Size  Used Avail Use% Mounted on
udev            441M     0  441M   0% /dev
tmpfs            90M  3.1M   87M   4% /run
/dev/sda1        63G  4.3G   56G   8% /
tmpfs           449M     0  449M   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
tmpfs           449M     0  449M   0% /sys/fs/cgroup
/dev/sda15      124M  262K  124M   1% /boot/efi
/dev/sdb1       3.9G   16M  3.7G   1% /mnt/resource
tmpfs            90M     0   90M   0% /run/user/1000
```



## 查看硬盘空间信息

```bash
$ sudo fdisk -l
```

Example Result:

```bash
aegir@0xday:~$ sudo fdisk -l
Disk /dev/sda: 64 GiB, 68719476736 bytes, 134217728 sectors
Disk model: Virtual Disk    
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes
Disklabel type: gpt
Disk identifier: BB042247-DA93-634A-8D04-FD99013BF2F9

Device      Start       End   Sectors  Size Type
/dev/sda1  262144 134217694 133955551 63.9G Linux filesystem
/dev/sda14   2048      8191      6144    3M BIOS boot
/dev/sda15   8192    262143    253952  124M EFI System

Partition table entries are not in disk order.


Disk /dev/sdb: 4 GiB, 4294967296 bytes, 8388608 sectors
Disk model: Virtual Disk    
Units: sectors of 1 * 512 = 512 bytes
Sector size (logical/physical): 512 bytes / 4096 bytes
I/O size (minimum/optimal): 4096 bytes / 4096 bytes
Disklabel type: dos
Disk identifier: 0x225ba861

Device     Boot Start     End Sectors Size Id Type
/dev/sdb1         128 8386559 8386432   4G 83 Linux
```





## 调整文件系统空间

扩容/压缩分区后重新加载文件系统大小

当文件系统被 `mount` 则只能扩容

```bash
$ resize2fs /dev/sda1
```

