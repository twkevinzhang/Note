# Win7虛擬機無法打開內核設備:\\Global\\vmx86
###### tags:`虛擬機` `windows` `win7` `error`
 參考至:
  - https://jingyan.baidu.com/article/3d69c5518b8bfef0cf02d7e1.html

### step.1

開始 - 運行（輸入CMD）- 確定或者Enter，打開管理員命令視窗；![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh4.googleusercontent.com/oqMI_q5659gx0MGfMKaSWNGyaQi1NzVgnMi6L_ZIa50JNVaD_mjxCJFKdjwZn1w0iFGF5fNFpzPpLp8y4WTxyB7I5ibGSMDh89oGQKVhQSR1q3ejL6Sb8AZw2KR3DnNDIhjI5dPk)

### step.2

我們先複製net start vmci，左鍵點擊管理員命令視窗左邊的小方框 - 編輯 - 粘貼，再按回車鍵（Enter）:

![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh3.googleusercontent.com/6WRrRamNIpgMT5cdqXU19m9O2zvfI-csWfAkwyGHHoGePcb14qZGS21nRJKJHn6xnLs-V37Y9HdZ2pcHgVy6ykgfgzKKQ9guf7O2U9fh-LPxNtpfG3Q8d5PZlB6k5FLZN7OPhbGi)

### step.3

可見：請求的服務已經啟動。再複製net start vmx86，左鍵點擊管理員命令視窗左邊的小方框 - 編輯 - 粘貼，再按回車鍵（Enter）;

![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh3.googleusercontent.com/IKgDzbtQuVLXN1d92Co-F0b0F9QoEViPI8DhVcfzQkNGaGJ6M6HUZTnzYlV-HMWs6rvTVlbr11olZjke_foRwcFVT2ctxqXj2DD3xrT6yqwiKXAw98-CBQPnLp1z7UkaKQRJ3hP6)

### step.4

我們按照上述方法，再依次輸入：

```
net start VMnetuserif

sc config vmci=auto

sc config vmx86=auto

sc config VMnetuserif=auto
```

並且每輸入一次，都要按一次回車鍵（Enter）;

我们按照上述方法，再依次输入：

```
net start VMnetuserif

sc config vmci=auto

sc config vmx86=auto

sc config VMnetuserif=auto
```

并且每输入一次，都要按一次回车键（Enter）;![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh3.googleusercontent.com/pD_qtXltdO7VPY16qGSzkrCkdtIhnrV9_jKFK6Zk9mzTMRgYBZ92WRi-J_8bdZ-dmfTpLtkUv__w3dTI--dqyrbM6ukNzK9coEZZhcWuOlBXR5TjwfTwW5CQWcuj4s_5n_-1WU59)

### step.5

如果無法運行命令，則從 VMware Workstation安裝目錄，找到 ：vmx86.sys（或者是vmx64.sys）和 vmci.sys檔， 複製：vmx86.sys和 vmci.sys文件；

![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh5.googleusercontent.com/Gqg3CgiazKtLHqDLC1k1DsGoSdgSRTzRKShwDJjk20pN_zKxuC8k9cmJfy6220h97eln4cOijiGQ22MveT3a0tOwtJ5kMG1ejqeNvXOw58VJzNCItehZSL4WhzIsNOSrrOy_rcff)

![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh3.googleusercontent.com/G25QF1v4QidKOiEdvUGBa7MntGEnp_ImfQ07xyTTLBLHxcb9oErxF-zQeXppwsmD_aLYDDeadR_Q_DZatz-jzsHJKbo8h1_WtjpVJ2MoYkFIpwpxuLk6rElQ1Pnzk3VACM1wQSH2)

### step.6

我們打開c:\windows\system32\drivers，把vmx86.sys和 vmci.sys文件粘貼進去；

![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh3.googleusercontent.com/8Bi0IiDHX-Wsse2GGoKNMIAMatcaVv3vyywjW76-S9hCmS-vsEhdH_Hq9wGevyDCDZZH9iH9kMqlxJ3G_fUrh5Skt35PQBxap-c6ZZVlSiU2R5_TbjI5ABV1MzKaDKy8UKH7Nkfx)

![Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://lh5.googleusercontent.com/wPtxjRkSrP44sype2FW-dOuMQH0Efl4t7VHW_Ok6tGf4OuM_XvB0MXcRSk88cjoHQMN4AN3CO-1yUv2YwpKCFZ89NqXL4LHA70v1p4edTvPGrl1VxWWYnQv8JqRj-ZK5-eV9ihp3)

### step.7

重新開機電腦。這樣操作後，問題應該能夠得到解決