# 將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)
##### tags:`Android` `降版` `Samsung` `root`
## 參考
 - [[梅問題教學網] 將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)](https://www.minwt.com/mobile/android/7364.html)

## 情境說明
as title

## 事前準備: 
 - 電腦須安裝[Samsung Kies](http://www.samsung.com/tw/support/usefulsoftware/KIES/JSP)
 - 請先將手機進行[Odin 3.0.7](http://forum.xda-developers.com/showthread.php?t=1722686)備份
 - [原廠韌體(台灣韌體BRI)](http://www.sammobile.com/firmwares/1/?model=GT-N7000&pcode=BRI#firmware)
 - [品質穩定的傳輸線](http://shopping.pchome.com.tw/?mod=item&func=exhibit&IT_NO=DGAS2W-A47201303)

## 步驟
### Step1
首先將手機關機後，再同時按住「音量＋鍵 + 電源鈕 + Home」不放。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/1.jpg)


### Step2
當出現這畫面時，放開所有按鍵，透過音量鍵可上下切換選項，電源是確定鍵，這時分別將wipe data/factory reset與wipe cache partition選項，按確定與YES，將手機清除回復原始狀態，都清好後，再選擇reboot system now重新開機。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/2.jpg)


### Step3
當重新開機後，再將手機關機，這時再按住按住「音量－鍵 + 電源鈕 + Home」不放，直到出現以下畫面。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/3.jpg)


### Step4

再按一下「音量+鍵」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/4.jpg)

### Step5
回到電腦開啟Odin3應用程式，接著點一下PDA鈕。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/5.jpg)


### Step6
選擇剛所下載的韌體，這邊要注意，韌體版本的型號要與手機相同才行，梅干當時沒注意到，搞了好久才發現，原來是韌體版本抓錯了。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/6.jpg)


### Step7
當韌體驗證完畢後，接著將手機與電腦連接。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/7.jpg)


### Step8
當連接成功時，在Odin的工作面板的，ID下方會亮藍色燈號，表示已抓到手機。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/8.jpg)


### Step9
這時再按Start鈕，就會開始進行刷機啦！

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/9.jpg)


### Step10

此時上方會看到刷機的進度，同時手機上，也會出現藍色的進度條，整個過程大約10分鐘左右。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/10.jpg)

### Step11

當面板出現PASS!，就表示己刷機完成，就可將連接線給拆除。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/11.jpg)

### Step12
這時會卡在SAMSUNG的畫面，別擔心將手機關閉，再執行一次步驟2。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/12.jpg)


### Step13

再重新開機後，大約會在SAMSUNG的畫面停個二分鐘左右，接著就會開始安裝Samsung的基本應用程式，裝完後就可順利的進到手機畫面啦！到系統看一下，哈～終於回到4.0.4的版本，這樣就不會再卡、頓、慢啦！

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/將Samsung-Galaxy-Note-Android4.1.2降刷回舊版不再卡、頓、慢(免root)/13.jpg)