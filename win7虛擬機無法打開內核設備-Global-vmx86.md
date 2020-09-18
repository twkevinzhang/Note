# win7虛擬機無法打開內核設備-Global-vmx86
###### tags:`vmware` `windows` `windows 7`
## 參考
  - [[baidu] Win7虚拟机无法打开内核设备:\\Global\\vmx86](https://jingyan.baidu.com/article/3d69c5518b8bfef0cf02d7e1.html)

## 錯誤描述:
打開vmware，啟動其中一台虛擬機時，出現以下錯誤:
> 无法打开内核设备“\\.\Global\vmx86”: 系统找不到指定的文件。你想要在安装 VMware Workstation 前重启吗?未能初始化监视器设备。

### step.1

開始 - 運行 (輸入CMD)- 確定或者Enter，打開管理員命令視窗；
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/1.jpg)

### step.2

我們先複製net start vmci，左鍵點擊管理員命令視窗左邊的小方框 - 編輯 - 粘貼，再按回車鍵 (Enter):

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/2.jpg)

### step.3

可見: 請求的服務已經啟動。再複製net start vmx86，左鍵點擊管理員命令視窗左邊的小方框 - 編輯 - 粘貼，再按回車鍵 (Enter);

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/3.jpg)

### step.4

我們按照上述方法，再依次輸入: 

```
net start VMnetuserif
sc config vmci=auto
sc config vmx86=auto
sc config VMnetuserif=auto
```

並且每輸入一次，都要按一次回車鍵 (Enter);

我们按照上述方法，再依次输入: 

```
net start VMnetuserif
sc config vmci=auto
sc config vmx86=auto
sc config VMnetuserif=auto
```

并且每输入一次，都要按一次回车键 (Enter)
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/4.jpg)

### step.5

如果無法運行命令，則從 VMware Workstation安裝目錄，複製 `vmx86.sys` (或者是`vmx64.sys`)和 `vmci.sys`文件；

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/5.jpg)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/6.jpg)
### step.6

我們打開`c:\windows\system32\drivers`，把`vmx86.sys`和 `vmci.sys`文件粘貼進去；

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/7.jpg)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/win7虛擬機無法打開內核設備-Global-vmx86/8.jpg)

### Fin.

重新開機電腦。這樣操作後，問題應該能夠得到解決