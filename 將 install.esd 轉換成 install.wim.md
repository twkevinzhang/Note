# 將 install.esd 轉換成 install.wim
###### tags:`重灌準備`
參考至:[http://blog.ilc.edu.tw/blog/index.php?op=printView&articleId=488747&blogId=25793](http://blog.ilc.edu.tw/blog/index.php?op=printView&articleId=488747&blogId=25793)

製作好的 ESD 安裝映像檔如果要修改的話，就要轉換成 WIM 檔，才能進行掛載及修改。

以下的做法參考：

[esd 及 wim 轉換問題](http://nonameteam.cc/thread-1786-1-1.html)

底下是進行的步驟：

1. 首先先建立三個子目錄，這裡以 C 磁碟機為例

![](https://lh4.googleusercontent.com/-5WRRxuHoilruOPTXw1FvxflxlReNvjJJ9yjI7z5HqpIYuRlY-CodpjlyytLB6PSIyiSk4-sDrFy2KiP0uOPGRkxEJWmf7OQkHLiuttMkgf2qXesLdcuEj3S-5s-y4BcuEjOw-rU)

`esd` 目錄是放置 `install.esd`

`temp` 目錄是轉換時的暫存目錄

`wim` 目錄是放置轉換完成的 `install.wim`

2. 將 `install.esd` 檔案的映像套用到指定的目錄，不過要特別注意的是 dism 的版本不能太舊，要 6.3.9600.16610 以上版本

目前我用的版本是 6.3.9600.17031 就是 Windows 8.1 Update 1 的版本

![](https://lh6.googleusercontent.com/T43avmwrMvNAXwgaW5PL6vArsLu5W6AjUeqtngXQ1wYyn7rn766Ps_MJwXvgpf8VoSBcd3hQ-69oZcESB-MNCr9u7z-p8foS8pNM9lSW3zvUhk6UtXVEruhWpVLgAgO6vZ8aR8IA)

`dism /apply-image /imagefile:c:\esd\install.esd /index:1 /applydir:c:\temp`

![](https://lh4.googleusercontent.com/_NoS1qhLnTPVV8XengNgEFIh-NF7UHqTyLOsc7NkVS6z3V5kLJcfDDPSf9fSTtpLtmqrLxbLY1SmYAu8ZGncyWgbSU4FW-LWr7xECIHJ58OxK4jRKxpFRFyPQ5BIqKoczTdHpN2f)

3. 檢查 temp 的目錄，可以發現目錄中的檔案及目錄，就是 `install.esd` 中的內容

![](https://lh5.googleusercontent.com/M0c6cIZAIyYQL2hN5exnn3mvTUpl0VEBeRwVwED1LImFSfrM1yMSAhg9BcEhSULO_UqV05FonrcboRgWUSaTyC2PGnoYR0m3qvcYDU9pgwdv8ov1mN7zNFHASQ4L-UPx1-yYQftE)

4.  將 temp 目錄中的檔案及目錄擷取成 install.wim

`dism /capture-image /imagefile:c:\wim\install.wim /capturedir:c:\temp\ /name:"Windows 8.1 標準版" /compress:max /checkintegrity /verify`

5. 執行完成後，可以執行下面指令來進行檢查，是否有轉換成功

`Dism /Get-ImageInfo /ImageFile:c:\wim\install.wim`

![](https://lh4.googleusercontent.com/0N_93WqzGtCeJIsHiKWH2j6ECWYFY-6llUR1-fbThHi9mobRpyd8rWnUB6PbIwdkczmCgniPCD60d7ZckQ1cVlp1aTwt5BxhiizcP6eY0gAB0rmDIJXpdNz1eGORhbAljqhfxP-U)