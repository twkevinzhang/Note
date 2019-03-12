# chrome-快取資料夾與使用者資料夾設定
###### tags: `瀏覽器` `chrome` `temp`

 參考至:[http://sppmsppm.blogspot.com/2015/02/chrome.html](http://sppmsppm.blogspot.com/2015/02/chrome.html)

這個方法就是將原來的預設路徑 改成指向你想要路徑的捷徑

 

在Linux上稱為symbolic link

在Windows上 用mklink建立 (用右鍵的建立捷徑似乎不行)

在開始打上cmd 並執行以下參數

```
mklink /D "C:\Users\XXXX\AppData\Local\Google\Chrome\User Data" "D:\ChromeUserData"

mklink /D "D:\ChromeUserData\Default\Cache" "R:\Temp"
```

我的設定方法是 將原來預設的User data目錄指向D槽

但是又想讓快取放在ramdisk裡 因此就加了第二條

把在D槽裡面的使用者資料夾下 快取的目錄 設定到ramdisk裡

這樣就完成了 Chrome瀏覽器使用者資料放在一般硬碟 快取放在ramdisk的設定

P.S.這邊有一點要注意的是 如果mklink指向的資料夾不存在

 

Chrome瀏覽器會砍掉那個捷徑然後自己新建資料夾

所以指向ramdisk的那個資料夾一定要在開機時建好

我是將windows的temp目錄也設定在ramdisk裡

所以開機才會在ramdisk裡生成Temp目錄

如果ramdisk開機不會生成任何資料夾的話 也可以直接指定R:就好

`mklink /D "D:\ChromeUserData\Default\Cache" "R:\"`