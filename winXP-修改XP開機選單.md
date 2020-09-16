# winXP-修改XP開機選單
###### tags:`windows` `開機選單`  `winXP`

參考至:
 - https://sites.google.com/site/yang198510/xp-kai-ji-xuan-dan-xiu-gai

我的電腦點滑鼠右鍵>內容>進階>啟動與修復(設定)>編輯(會開啟`BOOT.INI`)

    [boot loader]
    timeout=5

    default=multi(0)disk(0)rdisk(0)partition(1)\WINDOWS

    [operating systems]

    multi(0)disk(0)rdisk(0)partition(1)\WINDOWS="Microsoft Windows XP Professional" /noexecute=optin /fastdetect

這行以下都刪掉..然後儲存

`BOOT.INI`是XP的開機選單

`timeout=5` (開機選單等待5秒) 如果你只有一個開機系統~就不會出現開機選單

    default=multi(0)disk(0)rdisk(0)partition(1)\WINDOWS

開機選單的光棒固定會停留在哪一個選項(裝置0的第一個磁碟分割)

    multi(0)disk(0)rdisk(0)partition(1)\WINDOWS="Microsoft Windows XP Professional" /noexecute=optin /fastdetect

這邊是開機選單的內容~意思同上~其中的`="Microsoft Windows XP Professional"`是可以更改你喜歡的名稱

假如你有一個硬碟~分成C跟D..你把98裝在C之後~再裝XP到D

那麼上面就會變成有2行

    multi(0)disk(0)rdisk(0)partition(1)\WINDOWS="Microsoft Windows"

    multi(0)disk(0)rdisk(0)partition(2)\WINDOWS="Microsoft Windows XP Professional" /noexecute=optin /fastdetect

注意到`partition(1`)跟`partition(2)`...就是C跟D的意思