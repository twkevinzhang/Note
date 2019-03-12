# 無法透過 USB 裝置安裝 Windows 7
###### tags: `重灌` `win7` `windows` `重灌準備` `USB開機隨身碟`
 參考至:[https://www.gigabyte.com/tw/Support/FAQ/3459](https://www.gigabyte.com/tw/Support/FAQ/3459)

無法透過 USB 裝置安裝 Windows 7。

由於 Windows 7 未內建 Intel 100 系列晶片組 USB 驅動程式，請參考下列步驟安裝作業系統：

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

參考至:[http://gigabytedailycht.blogspot.com/2015/08/100windows-7-usb.html](http://gigabytedailycht.blogspot.com/2015/08/100windows-7-usb.html)

前些日子，我們發表了一篇如何將XHCI驅動程式包進Windows 7 USB安裝碟，讓它可以安裝在100系列平台的[教學文章](http://gigabytedailycht.blogspot.tw/2015/08/100windows-7-usb.html)。雖然筆者已經盡量將步驟以白話文呈現了，但是整個流程還是落落長，而且又要解壓縮、又要建立資料夾，又要下指令的...感覺就不是那麼容易親近。讓大家不禁在心裡大喊，難道沒有更簡單的方法嗎？？？

有的，大家可使用技嘉最新上傳到官網的Windows Image Tool 這個工具軟體

[http://download.gigabyte.us/FileList/Utility/mb_utility_windowsimagetool_z370.zip](http://download.gigabyte.us/FileList/Utility/mb_utility_windowsimagetool_z370.zip)

它可以讓您在幾個步驟內，輕鬆建立已經將XHCI驅動程式包進Windows 7 已經的USB安裝碟，讓您輕鬆達成想要的目的！

Windows Image Tool 是免安裝的綠色程式，您從技嘉官網下載之後，解壓縮並點選資料夾中的執行檔，便可以看到如下的應用程式主畫面，整個選項跟UI相當簡約：

![](https://lh4.googleusercontent.com/f2eT7RyS3oI2i0G3oQdkb0AO1h5JdOXGpaJcRg41rkp26iUC_f8QQ1ryseWkNr9thOD_Tykaa4pLO2IYmEnxffek7RJr0QzI0yeTHI3990ffB4X88p2khKmnlBLu1Y9IGGZlRKpW)

其中Source Path是指您OS的來源，可以是光碟片（以本文為例，是H:\）、虛擬光碟載入的ISO檔（以本文為例，是K:\），甚至如果您有一個已經做好，但還沒包入XHCI驅動程式的Windows 7 USB安裝碟，技嘉的Windows Image Tool也可以幫您把XHCI驅動程式包進去（要使用這個功能請選擇None-Add USB drivers這個選項）

當然，您也可以單純只用Windows Image Tool 這個工具軟體來製作USB安裝碟，而不將XHCI驅動程式包進去，只要將"Add USB drivers to an offline Windows 7 image"的勾選取消，Windows Image Tool 就會在不包入XHCI驅動程式的情況下，製作USB安裝碟。

![](https://lh4.googleusercontent.com/lrdOW2Bdk0l1jyHj8ZTGxpu4teota-8Wd0tvQVnK56zISsF55Ptxl3JfupPNHrhy62NgXH6YaGbVn7qs2YfkmynFGgg9LzRHs4e6U6g61fh5htwjrQ-_7OM4Q-n82xtjxwGa2E3a)

選完OS來源之後，接下來就選擇您要用來做安裝碟的USB裝置，請選用容量超過4GB的USB隨身碟，以便有足夠的空間製作Windows 7安裝碟。

![](https://lh6.googleusercontent.com/qWNkGJX3zN802ZXHcVcW1bw19ZH5F3u_5N4HYufaKkKr-yeBGHZehJNm_ulivnwjELSXYLqfQQlmrYZiFSY6qsGgvVRE_LdDGKzM_jLDBZYQ9_hVw0qsQk2E0A4TvKyPDFwO9hwA)

OS來源跟USB裝置都選擇好了之後，按下Start按鍵，接下來給您的電腦一點時間，讓它把讓它把USB安裝碟做好，這樣您就可以用它將Windows 7安裝在100系列平台囉！