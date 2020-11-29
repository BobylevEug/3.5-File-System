# 3.5-File-System

## 4. https://losst.ru/komanda-fdisk-v-linux

## 5. http://rus-linux.net/kos.php?name=/papers/part/2.html

## 6,7. https://www.dmosk.ru/miniinstruktions.php?mini=mdadm

## 8-13. https://losst.ru/sozdanie-i-nastrojka-lvm-linux

## 14.

vagrant@vagrant:~$ lsblk
NAME                        MAJ:MIN RM  SIZE RO TYPE  MOUNTPOINT
sda                           8:0    0   64G  0 disk
├─sda1                        8:1    0  512M  0 part  /boot/efi
├─sda2                        8:2    0    1K  0 part
└─sda5                        8:5    0 63.5G  0 part
  ├─vgvagrant-root          253:0    0 62.6G  0 lvm   /
  └─vgvagrant-swap_1        253:1    0  980M  0 lvm   [SWAP]
sdb                           8:16   0  2.5G  0 disk
├─sdb1                        8:17   0    2G  0 part
│ └─md1                       9:1    0    2G  0 raid1
│   └─vol_grp1-logical_vol0 253:2    0  100M  0 lvm   /tmp
└─sdb2                        8:18   0  511M  0 part
  └─md0                       9:0    0 1018M  0 raid0
sdc                           8:32   0  2.5G  0 disk
├─sdc1                        8:33   0    2G  0 part
│ └─md1                       9:1    0    2G  0 raid1
│   └─vol_grp1-logical_vol0 253:2    0  100M  0 lvm   /tmp
└─sdc2                        8:34   0  511M  0 part
  └─md0                       9:0    0 1018M  0 raid0

## 18. 
vagrant@vagrant:~$ cat /proc/mdstat
Personalities : [linear] [multipath] [raid0] [raid1] [raid6] [raid5] [raid4] [raid10]
md0 : active raid0 sdc2[1] sdb2[0]
      1042432 blocks super 1.2 512k chunks

md1 : active raid1 sdc1[1] sdb1[0]
      2094080 blocks super 1.2 [2/2] [UU]

unused devices: <none>
