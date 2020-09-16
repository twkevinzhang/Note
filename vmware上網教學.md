# vmware上網教學
###### tags: `虛擬機` `vmware` `網路`
## 參考
  - [[xuite] 解決VMWare不能上網](http://blog.xuite.net/r413318/justforfun/35138059-[分享]解決VMWare不能上網)

## 情境說明
簡單的說就是讓我們可以上網的那個IP分享網路給VMWare用 ，這樣VMWare也就能透過那個可以上網的IP上網了!!
以下是在Windows XP SP2  和 VMWare6 下操作，理論上VMWare6版本以上都可以

## 步驟
### step1.

先設定VMWare，先到這個畫面，點選Ethernet，來設定。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/1.png)

### step2.

選擇Cutstom: Specific virtual network，並且選擇VMnet8(NAT)這個選項，選好後按確定。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/2.png)

### step3.

我們去網路連線 (網路芳鄰->內容)，選擇 區域連線->內容。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/3.png)
### step4.

切換到進階標籤，並且把「允許其他使用者透過這台電腦的網際網路連線來連線」勾選起來，在把家用網路連線設定為「VMWare Network Adapter VMnet8」，之後按下確定。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/4.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/5.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/6.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/7.png)

之後這邊會跑出這個訊息，請不用在意它，按下確定。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/8.png)


在這時候，我們的區域連線就會多出一隻手，表示開始分享網路。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/9.png)

### step5.

選擇VMWare Network Adapter VMnet8 -> 內容，再選擇Internet Protocal(TCP/IP)這個選項，會看到IP位址與子網路遮罩都被設定了。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/10.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/11.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/12.png)

### step6.

把IP位址改成192.168.55.1 (55可以為任意值)，子網路遮罩就不用改，慣用DNS伺服器給改成168.95.1.1 (這是中華電信的DNS)，設定完後按確定。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/13.png)

設定到這步基本上NAT就算架設完成了!! 再來我們去VMWare裡面的作業系統做些設定。

> 注意::  下面是在VMWare操作

### step7.

我們去網路連線 (網路芳鄰->內容)，選擇 區域連線->內容，並選擇Internet Protocal(TCP/IP)這個選項。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/14.png)
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/15.png)
### step8.

把IP設定為192.168.55.5 (55就是剛剛給的值，最後的5可以為任意值)，子網路遮罩為255.255.255.0，預設閘道為192.168.55.1，慣用DNS伺服器為168.95.1.1，按下確定就大功告成!!
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/vmware上網教學/16.png)


設定就到這邊結束，VM可以上網囉!!!!!