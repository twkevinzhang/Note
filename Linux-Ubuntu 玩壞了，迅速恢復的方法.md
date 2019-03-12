# Linux-Ubuntu 玩壞了，迅速恢復的方法
###### tags: `Linux` `Ubuntu` `error` `還原`
 參考至:http://ahhafree.blogspot.com/2014/03/ubuntu_12.html

注:  [ezgo](http://ezgo.westart.tw/ezgo11/) 是臺灣的一群好手依 Ubuntu 重製的適合切學到高手都方便學習和使用的 Ubuntu免費系統

#### Step1.

用ubuntu/ezgo live CD/隨身碟 開機

（建議：若是您是剛開始玩 ezgo 或 Ubuntu ；第一次安裝好ezgo後，用系統內定的軟體製作一個 ezgo live CD或ezgo live 隨身碟。以備不時之需，雖然可能用不到！）

　（心得：經過多次重灌 Ubuntu 後，每次用 live USB隨身碟 重新安裝系統都感覺好爽。因為以前在安裝 M$ Windows 實在耗時－－系統裝完＋驅動程式＋常用軟體＋雜七雜八，得至少半天以上－－若很閒倒是殺時光的好方法，而且因為要常換安裝片，人還不可以跑開；新買的電腦有新系統還原備份尚堪忍受。但用 live USB隨身碟 重新安裝Ubuntu系統 ，不到一個小時，全部ＯＫ，只要前面幾個步驟做好，就可以泡杯咖啡、到處逛了，四十分鐘後回來，重開機，就ＯＫ了^^，常用軟體也裝好了，可以開始玩了，讚！－－輸入法得看個人喜好來裝喔！）

#### Step2.

連上網路

#### Step3.

終端機輸入

sudo add-apt-repository ppa:yannubuntu/boot-repair && sudo apt-get update

#### Step4.

sudo apt-get install -y boot-repair && (boot-repair &)

會跳出 boot-repair的視窗(中文)

#### Step5.

按使用建議修復，一鍵完成!

-------------------------------------------------------------

[help ubuntu 網站](https://help.ubuntu.com/community/Boot-Repair#Recommended_repair)上亦有如下的說明：

# Getting Boot-Repair

## 1st option : get a CD including Boot-Repair

The easiest way to use Boot-Repair is to burn one of the following disks and boot on it.

*   [Boot-Repair-Disk](http://sourceforge.net/p/boot-repair-cd/home) is a CD starting Boot-Repair automatically.

*   Boot-Repair is also included in [Linux-Secure-Remix](https://help.ubuntu.com/community/LinuxSecureRemix).

Remark : you can also install the ISO on a [live-USB](https://help.ubuntu.com/community/Installation/FromUSBStick) (eg via [UnetBootin](http://unetbootin.sourceforge.net/) or [LiliUSB](http://www.linuxliveusb.com/) or [Universal USB Installer](http://www.pendrivelinux.com/universal-usb-installer-easy-as-1-2-3/)).

## 2nd option : install Boot-Repair in Ubuntu

- [boot your computer on a Ubuntu live-CD or live-USB.](https://help.ubuntu.com/community/BootFromCD)

- choose "Try Ubuntu"

- connect to the Internet

- open a new [Terminal](https://help.ubuntu.com/community/Terminal), then type:

sudo add-apt-repository ppa:yannubuntu/boot-repair && sudo apt-get update

- Press ENTER.

- Then type:

sudo apt-get install -y boot-repair && (boot-repair &)

- Press ENTER

注:當然，除非連開機都不行了，否則建議您安裝好後，先建立三四個使用者，都給他管理者權限（★不要設定免密碼自動登入，好處多多，不要嫌麻煩－－最大好處就是玩爛一個user，可以方便的改為下一個user，還有別人想動您的電腦，怎麼也不行），這樣一個使用者玩爛了，就進入下一個使用者玩，等玩壞四個使用者，您早就很熟悉這個好玩的系統了！