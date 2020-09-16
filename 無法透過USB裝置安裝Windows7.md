# 無法透過USB裝置安裝Windows7
###### tags: `windows 7` `USB 開機隨身碟` `重灌準備`
## 錯誤描述:
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/無法透過USB裝置安裝Windows7/1.png)

## 原因: 
Windows 7 未內建 Intel 100 系列晶片組 USB 驅動程式

## 解決: 
請參考下列步驟安裝作業系統: 

1.  準備一個 USB 隨身碟，至微軟官方網站製作 Windows 7 正版 USB 安裝碟。

2.  至技嘉官方網站下載 Windows USB Installation Tool。

3.  解壓縮該工具並執行 WindowsImageTool。

1.  確認已插入製作完成的 USB 安裝碟。

2.  Source Path 請選取 None-Add USB drivers。

3.  Destination Path 請選擇稍早製作的 Windows 7 正版 USB 安裝碟。

4.  點擊 [Start] 開始執行，結束後按 [Close] 離開。

5.  將製作好的 USB 安裝碟插入需要安裝 Windows 7 的電腦。

6.  開機後按 [F12]，選擇欲使用的開機裝置 (Windows 7 正版 USB 安裝碟) 即可開始安裝 Windows 7。

詳細步驟可參考[此連結](http://gigabytedailycht.blogspot.tw/2015/09/windows-image-tool-win-7100.html)。

## 參考: 
- https://www.gigabyte.com/tw/Support/FAQ/3459
- [gigabyte blog](http://gigabytedailycht.blogspot.com/2015/08/100windows-7-usb.html)