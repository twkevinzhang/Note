# 開機出現bootmgr-is-missing
###### tags:`windows` `開機錯誤`

## 參考
 - [[pixnet] 開機出現 bootmgr is missing (win 7)](http://bacat.pixnet.net/blog/post/38678181-開機出現-bootmgr-is-missing-(win-7))

## 原因: 

1. 沒有安裝作業系統

2. 有安裝作業系統，但硬碟中放系統的那塊磁區剛好壞掉

## 解決: 
### 方法1:

放W7安裝片修復後，選擇自動修復

### 方法2:

放W7安裝片修復，進入命令提示字元來輸入指令自行重建開機檔

```
Bootrec /FIXBOOT
Bootrec /FIXMBR
```

### 方法3:

利用diskpart轉換成NTFS

 - 放W7安裝片修復時選擇<進入命令提示字元>
 - 輸入`diskpart` 按ENTER
 - 輸入`LIST DISK` 看現在接在電腦的磁碟代號
 - 輸入`select disk` (數字) 選擇出問題的那顆硬碟 圖例是磁碟3
 - 輸入`clean` 將這顆硬碟完全清除 注意:是將<這顆硬碟>全部清掉 回復到新買還需要重新分割和格式化的狀態

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/開機出現bootmgr-is-missing/1.png)