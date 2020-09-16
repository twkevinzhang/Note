# 將install.esd轉換成install.wim
###### tags:`重灌準備`
## 參考
 - [[edu] 將install.esd轉換成install.wim](http://blog.ilc.edu.tw/blog/index.php?op=printView&articleId=488747&blogId=25793)
 - [esd 及 wim 轉換問題](http://nonameteam.cc/thread-1786-1-1.html)

## 情境說明
製作好的 ESD 安裝映像檔如果要修改的話，就要轉換成 WIM 檔，才能進行掛載及修改。

## 步驟

首先先建立三個子目錄，這裡以 C 磁碟機為例

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將install.esd轉換成install.wim/1.png)

 - `esd` 目錄是放置 `install.esd`
 - `temp` 目錄是轉換時的暫存目錄
 - `wim` 目錄是放置轉換完成的 `install.wim`

將 `install.esd` 檔案的映像套用到指定的目錄，不過要特別注意的是 dism 的版本不能太舊，要 6.3.9600.16610 以上版本

目前我用的版本是 6.3.9600.17031 就是 Windows 8.1 Update 1 的版本

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將install.esd轉換成install.wim/2.png)

`dism /apply-image /imagefile:c:\esd\install.esd /index:1 /applydir:c:\temp`

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將install.esd轉換成install.wim/3.png)

檢查 temp 的目錄，可以發現目錄中的檔案及目錄，就是 `install.esd` 中的內容

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將install.esd轉換成install.wim/4.png)

將 temp 目錄中的檔案及目錄擷取成 install.wim

`dism /capture-image /imagefile:c:\wim\install.wim /capturedir:c:\temp\ /name:"Windows 8.1 標準版" /compress:max /checkintegrity /verify`

執行完成後，可以執行下面指令來進行檢查，是否有轉換成功

`Dism /Get-ImageInfo /ImageFile:c:\wim\install.wim`

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將install.esd轉換成install.wim/5.png)