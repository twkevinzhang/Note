# 在GCP-VM中使用桌面
###### tags:`GCP` `Linux` `remote` `Google(其他關鍵字)

## 參考
 - [[github.io] 在GCP開啟Ubuntu遠端桌面](https://infinitewing.github.io/2017/08/13/20170813001/)
 - [[github.io] GCP-防火牆](https://snoopy30485.github.io/2018/06/20/GCP-防火牆/)
 - [[blogspot] Setup GUI Desktop on Google Cloud Platform (GCP) VM instance](http://leadtosilverlining.blogspot.com/2019/01/setup-desktop-environment-on-google.html)
 - [Getting started with Vim: The basics](https://opensource.com/article/19/3/getting-started-vim)
 - [[csdn] 【Rayeager PX2分享】启动tightvncserver失败解决办法](https://blog.csdn.net/u010854102/article/details/45095017)

## 情境說明
用vnc的方式遠端使用GCP-VM，透過vnc的config就能設置桌面

## 事前準備
 - GCP VM, OS: Ubuntu 16
 - 安裝[VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/)，不是VNC Server

## 步驟
### GCP防火牆
1. 先進入 VPC 網路 → 防火牆規則
 ![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/31.png)

2. 點選建立防火牆規則後，參考以下設定
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/311.PNG)
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/312.PNG)
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/313.PNG)

3. 記得將網路標籤加入VM，設定才會生效(除非你在防火牆中的「目標」選「網路中的所有執行個體」)
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/314.PNG)

## 在Ubuntu上安裝元件
1. 進入文字終端模式後，複製貼上以下指令：
```
$ sudo apt-get update
$ sudo apt-get install gnome-core
$ sudo apt-get install vnc4server

$ vncserver
```
上述指令說明如下：

 - 更新套件庫資訊
 - 安裝gnome-core
 - 安裝vnc4server
 - 啟動vncserver，第一次啟動時會詢問設定密碼(如圖)，之後使用此密碼即可登入遠端桌面
 ![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/1.PNG)
  > 圖 第一次啟動時會詢問設定密碼

2. 打開VNC Viewer，試著連線看看
 ![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/21.PNG)
  > 圖 新增一個連線
  
 ![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/22.PNG)
  > 圖 第一階段完成!!

## 設定.vnc/xstartup
1. 輸入`vim .vnc/xstartup`來修改`.vnc/xstartup`成以下內容：
```
#!/bin/sh
# Uncomment the following two lines for normal desktop:
unset SESSION_MANAGER
# exec /etc/X11/xinit/xinitrc
#[ -x /etc/vnc/xstartup ] && exec /etc/vnc/xstartup
#[ -r $HOME/.Xresources ] && xrdb $HOME/.Xresources
#xsetroot -solid grey
#vncconfig -iconic &
#x-terminal-emulator -geometry 80x24+10+10 -ls -title "$VNCDESKTOP Desktop" &
#x-window-manager &
metacity &
gnome-settings-daemon &
gnome-panel &
```
輸入`:x!`儲存並退出

如不會使用vim，可參考[這篇](https://opensource.com/article/19/3/getting-started-vim)

2. 重新打開vncserver服務
```
$ vncserver
```
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/2.PNG)
  > 圖 重新打開vncserver服務

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/fin.PNG)
  > 圖 再次用VNC Viewer連線後

## 錯誤1: 連線後出現灰色的點點畫面，沒有Applications bar
### 錯誤描述:
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/err1.PNG)

### 解決
 - 輸入以下指令以重新安裝桌面相關套件:
 ```
 $ sudo apt-get install --reinstall ubuntu-desktop gnome-panel gnome-settings-daemon metacity nautilus gnome-terminal
 ```

### 參考
 - [[Stack Exchange] Unable to start gnome-terminal via VNC](https://askubuntu.com/questions/1206358/unable-to-start-gnome-terminal-via-vnc)

## 錯誤2: 想要用sudo啟動vncserver卻失敗
### 錯誤描述:
 輸入`sudo vncserver`卻出現`vncserver: Wrong type or access mode of /home/username/.vnc.`，如圖:
 ![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/err2.png)
### 解決
   - 修改root的密碼

    sudo passwd root

   - 依指示輸入兩次密碼
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/err22.jfif)
   - 用sudo啟動vncserver

    su - root bash -c "vncserver :1"

   - 輸入兩次登入密碼
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/err23.png)

   - 完成
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/在GCP-VM中使用桌面/fin.PNG)
### 參考
 - [[csdn] 【Rayeager PX2分享】启动tightvncserver失败解决办法](https://blog.csdn.net/u010854102/article/details/45095017)
