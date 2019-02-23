# Android Studio-Error while Installing APKs
 參考至:[https://dotblogs.com.tw/jgame2012/archive/2012/04/06/71311.aspx](https://dotblogs.com.tw/jgame2012/archive/2012/04/06/71311.aspx)

#### 如下問題:

Error while Installing APKs

#### 解決辦法:

1. 開啟命令提示字元(cmd)

2. 設定當前目錄路徑為你的Android SDK的目錄下有個platform-tools資料夾

(假設我的資料夾路徑為C:\android sdk\platform-tools\ ，則指令輸入cd C:\android sdk\platform-tools\)

3. 輸入adb kill-server

4. 再輸入adb start-server

5. 若看到

*daemon not running. starting it now on port 5037 *

*daemon started successfully *

6. 則表示成功，若看到

*daemon not running. starting it now *

ADB server didn't ACK

*failed to start daemon *

則可以開啟工作管理員查看是否有處理程序是adb.exe的，把這個處理程序關閉即可，

若沒有adb.exe這個處理程序的話，建議直接重開機，這樣也能關閉ADB server程序。

重開機後，再將上面的步驟做一遍，就可以看到成功訊息，之後開心使用Android Studio唄。

        如果還是不行:

1. 開啟Android Studio

2. 點擊Build>Clean Project

3. 點擊Build>Rebuild Project

4. 再將上面的步驟做一遍