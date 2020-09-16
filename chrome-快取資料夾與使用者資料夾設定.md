# chrome-快取資料夾與使用者資料夾設定
###### tags: `瀏覽器` `chrome` `temp`

## 參考
  - [[blog] Chrome快取資料夾與使用者資料夾設定](http://sppmsppm.blogspot.com/2015/02/chrome.html)

## 情境說明
這個方法就是將原來的預設路徑 改成指向你想要路徑的捷徑

在Linux上稱為symbolic link

在Windows上 用mklink建立 (用右鍵的建立捷徑似乎不行)

## 步驟
1. 在開始打上cmd 並執行以下參數

`mklink /D "C:\Users\XXXX\AppData\Local\Google\Chrome\User Data\Default\Cache" "R:\Temp"`

這樣就完成了 Chrome瀏覽器使用者資料留在原處，但其中的快取放在R:\Temp (ramdisk)的設定

## 認識與注意: 
如果mklink指向的資料夾不存在

Chrome瀏覽器會砍掉那個捷徑然後自己新建資料夾。

如果ramdisk開機不會生成任何資料夾的話 也可以直接指定R:就好

`mklink /D "D:\ChromeUserData\Default\Cache" "R:\"`