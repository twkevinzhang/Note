# VirtualBox-分享資料夾
###### tags:`VirtualBox` `虛擬機` `共用資料夾`
## 參考
  - [[blog] VirtualBox 分享資料夾](http://mh-resource.blogspot.com/2012/02/virtualbox-xp.html)

## 情境說明
有使用過虛擬電腦的一定知道Oracle VirtualBox這款虛擬機器軟體，VirtualBox能夠安裝多個客戶端作業系統，不過主端作業系統與客戶端作業系統想要互相分享資料該怎麼辦呢?這時就要分享資料夾的功能，此資料夾就像是一個門，連接虛擬電腦與主端電腦，藉由分享資料夾的功能來交換檔案

## 步驟
 - 首先，你得先安裝客端額外功能(Guest Addtions)，當開啟虛擬電腦後，點選上方的"裝置"，選擇"安裝Guest Addtions"

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/1.png)

 - 安裝完畢後，也是點選上方的"裝置"，選擇"共用資料夾"

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/2.png)

 - 再按右上角的"加入共用資料夾"

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/3.png)

 - 下拉"資料夾路徑"的選單，點選"其他"

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/4.png)

 - 選擇你要分享的資料夾

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/5.png)

若常常要開啟此資料夾，記得勾選"永久性"，並記住"你的資料夾名稱"，等等要輸入用

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/6.png)

 - 勾選"永久性"的資料夾會被分到"機器資料夾"，反之，則會分類到"瞬變資料夾"

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/7.png)

 - 但如此還是不能連結資料夾，請在虛擬XP裡開啟"命令提示字元"(視窗鍵+R)，並輸入`net use Z: \\vboxsvr\輸入你的資料夾名稱`

Z可更改成你想要的磁碟名稱，例如:A, B, M, N... 等等，此時就會看到多一個Z槽的網路磁碟

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/VirtualBox-分享資料夾/8.png)