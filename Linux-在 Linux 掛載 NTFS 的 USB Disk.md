# Linux-在 Linux 掛載 NTFS 的 USB Disk
###### tags: `Linux` `NTFS`
 參考至:
  - https://snippetinfo.net/media/238

先到以下網址下載最新的 source code

http://www.tuxera.com/community/ntfs-3g-download/

傳到 Linux 上之後，就解開，並執行以下動作：
`./configure make  make install # or  'sudo make install' if you aren't root`


等安裝好後，可以透過 fdisk -l 找出該 USB Disk 中的 代號

    [root@www mnt]# fdisk -l
    
    Disk /dev/sda: 500.1 GB, 500107862016 bytes
    255 heads, 63 sectors/track, 60801 cylinders
    Units = cylinders of 16065 * 512 = 8225280 bytes
    
    Device Boot      Start         End      Blocks   Id  System
    /dev/sda1   *           1          13      104391   83  Linux
    /dev/sda2              14       60801   488279610   8e  Linux LVM
    
    Disk /dev/sdb: 500.1 GB, 500105740288 bytes
    255 heads, 63 sectors/track, 60801 cylinders
    Units = cylinders of 16065 * 512 = 8225280 bytes
    
    Device Boot      Start         End      Blocks   Id  System
    /dev/sdb1               1       60802   488383488    7  HPFS/NTFS

在我的環境中，該 USB 的設備路徑為 /dev/sdb1。所以只要下 mount 就完成囉!
> mount -v -t ntfs-3g /dev/sdb1 /mnt/usb`

