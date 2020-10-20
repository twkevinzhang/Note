# 用wifi連接手機debug
###### tags:`android` `adb`

## 參考
 - [[pixnet] [Android] debug不用線，用ADB連接3G/wifi手機](https://j796160836.pixnet.net/blog/post/29108155)
 - [[blog] Android Wi-Fi debug功能](http://blog.alenshiun.tw/2016/05/android-wi-fi-debug.html)

## 情境說明
教你debug不用線，用3G或wifi直接無線Deploy程式

## 事前準備
 - 曾經連接過USB、做過開發設定的手機

## 步驟
1. 先確定手機有電，3G或Wifi的網路有開
1. 用 USB 傳輸線接上你的手機
1. 找到Android SDK的路徑 platform-tools/ 資料夾路徑，每個人裝位置因作業系統或個人喜好的都不太一樣，我的在`C:\Users\nesl\AppData\Local\Android\Sdk\platform-tools`
1. 開啟`cmd`，切換到Android SDK的路徑`cd C:\Users\nesl\AppData\Local\Android\Sdk\platform-tools`
1. 輸入`adb tcpip 5555`
1. 透過adb指令找到Android裝置的IP位置，輸入`adb shell ifconfig`
1. (可選)可以脫離USB連線了
1. 輸入`adb connect 192.168.1.3:5555`，中間換成你手機的IP位址

## 補充
 - 關閉Wi-Fi debug功能: `adb usb restarting in USB mode`
