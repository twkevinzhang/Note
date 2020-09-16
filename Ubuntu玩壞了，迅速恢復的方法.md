# Ubuntu玩壞了，迅速恢復的方法
###### tags: `Linux` `Ubuntu` `error` `還原`

## 參考
 - [[blog] Ubuntu 玩壞了，迅速恢復的方法－－盡力去玩吧！](http://ahhafree.blogspot.com/2014/03/ubuntu_12.html)
 - [[doc] help.ubuntu](https://help.ubuntu.com/community/Boot-Repair#Recommended_repair)上亦有如下的說明: 

## 事前準備
 - ubuntu/ezgo live CD/隨身碟

### Step1.用ubuntu/ezgo live CD/隨身碟 開機

### Step2.連上網路

### Step3.終端機輸入
`sudo add-apt-repository ppa:yannubuntu/boot-repair && sudo apt-get update`

### Step4.
`sudo apt-get install -y boot-repair && (boot-repair &)`

會跳出 boot-repair的視窗(中文)

### Step5.

按使用建議修復，一鍵完成!

-------------------------------------------------------------

[help ubuntu 網站](https://help.ubuntu.com/community/Boot-Repair#Recommended_repair)上亦有如下的說明: 

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

注:當然，除非連開機都不行了，否則建議您安裝好後，先建立三四個使用者，都給他管理者權限 (★不要設定免密碼自動登入，好處多多，不要嫌麻煩－－最大好處就是玩爛一個user，可以方便的改為下一個user，還有別人想動您的電腦，怎麼也不行)，這樣一個使用者玩爛了，就進入下一個使用者玩，等玩壞四個使用者，您早就很熟悉這個好玩的系統了！