# 將Samsung Galaxy Note Android4.1.2降刷回舊版不再卡、頓、慢（免root）
###### tags:`Android` `降版` `Samsung` `Note` `root`
 參考至:[https://www.minwt.com/mobile/android/7364.html](https://www.minwt.com/mobile/android/7364.html)

#### 準備工具：

*   [Samsung Kies](http://www.samsung.com/tw/support/usefulsoftware/KIES/JSP)

*   [Odin 3.0.7](http://forum.xda-developers.com/showthread.php?t=1722686)

*   [原廠韌體(台灣韌體BRI)](http://www.sammobile.com/firmwares/1/?model=GT-N7000&pcode=BRI#firmware)

*   [品質穩定的傳輸線](http://shopping.pchome.com.tw/?mod=item&func=exhibit&IT_NO=DGAS2W-A47201303)

#### 注意事項：

1.  請先將手機進行備份

2.  電腦須安裝Samsung Kies

3.  電量充足

#### Step1

![](https://lh3.googleusercontent.com/8Tkw-KsmNQMiz2-UhpnZuwsp31Gguqzn8mXM-MYgVnaI4K-HnY5CvuS0JAatBHeNqRi2ItgOxPflnDCVFZzkEnI9sT4vY9PxPhhQsZft2vhOycgBwiXXBeOX1GvAH6FtS9VhRlNX)

首先將手機關機後，再同時按住「音量＋鍵 + 電源鈕 + Home」不放。

#### Step2

![](https://lh3.googleusercontent.com/iI-TuEaTAY1ozDV7UKCxxdZ3rdFE50vV_tYnCkdrbyEfnY95KCEvZN6F_92WHs0wrUU7ODs9mUuuw9Hj-r6nRNMeeNM63rp_EEjE6t96SyMnFSQQFkz2_VgePuhbYQ_ROntJHnXx)

當出現這畫面時，放開所有按鍵，透過音量鍵可上下切換選項，電源是確定鍵，這時分別將wipe data/factory reset與wipe cache partition選項，按確定與YES，將手機清除回復原始狀態，都清好後，再選擇reboot system now重新開機。

#### Step3

![](https://lh4.googleusercontent.com/d4rz9drrLGdK0fOzzG5khL7lBe5GYhcTHtSl3B6GMBhDsR8kc4IJSvUiy_HGI2J7SUbX87oTF0fQku4R_cS03vk_IczAZnqf3sisWBpK6GbXLVHhP7OEoPnui4__1C0LbndWIQtc)

當重新開機後，再將手機關機，這時再按住按住「音量－鍵 + 電源鈕 + Home」不放，直到出現以下畫面。

#### Step4

再按一下「音量+鍵」。

![](https://lh3.googleusercontent.com/ZGClLlQW94pB0nislCm7soHbEd1tPZkPtn4lrUuWj95dfej9iItPyiJZOzCDeRGGWJRQ1L8PG4fgVFl9Ab_NQpYYnXcsS-27hAecHbShuXC3mtuYaCFNBu8fMrmwTSkVuJJSIovn)

#### Step5

![](https://lh5.googleusercontent.com/A96fTnZw93ClPy_GL_5ReeQ9M_mXNH19Ri5bOkVz9obBZPzgqYw8McwlmNOjI_0tODfMsIdiJEVNeQDs811ce-eSkBPQKYsxm1ubt0kB9cXgSn6Zftwc2Obe1OAXtI5jM7eJ0sw-)

回到電腦開啟Odin3應用程式，接著點一下PDA鈕。

#### Step6

![](https://lh3.googleusercontent.com/RFHlrkw561iKGEip-45AAMozdCQY9llR0eE2KJYVmdUIOs4gx1UEKrL33reiRvBQI54tf6kqVH98cljFNF-C4efncsMlbcFiL-GfMq1liwxSvns0vXu2GeEVwOmyKK56vEpycpTf)

選擇剛所下載的韌體，這邊要注意，韌體版本的型號要與手機相同才行，梅干當時沒注意到，搞了好久才發現，原來是韌體版本抓錯了。

#### Step7

![](https://lh3.googleusercontent.com/iOc9M6Xim8M-iHHqHNu9c4-MSLYtoDg2-nWzjB5kHy-T0aVlo68uBqaUuq9nATyDO9gC23XCJORT9DA24tevgKihuyvNKBQKrxIMVNj0HCj1gviaTfNQxTalhI-dh1QEUPr8O_gg)

當韌體驗證完畢後，接著將手機與電腦連接。

#### Step8

![](https://lh3.googleusercontent.com/5QoptCdZAs6F1YY1dkHLJvBgAgPAgPO0FOCqenHcy2ZOJQix93KvhLAkZfxxIfgq1lpZhwPtp5jJUgCx9C61cz19ONuTyjfMK7spAdYjZr2WRYXVj3DcRC71gRw4q-kzJ8U6VJA5)

當連接成功時，在Odin的工作面板的，ID下方會亮藍色燈號，表示已抓到手機。

#### Step9

![](https://lh4.googleusercontent.com/zdwAbbBop7jRbGpXAbSPdq2oll0ddVepC1uptnEpuRMZyfjq1IGA4aYgFJROG78PyfZ_eJM8Qq__2OPPTVDiAEVpwlnGY-NgJr49GgOqwCJyDFCjTJVt1yEN6bnM-tRL8-4TNeSc)

這時再按Start鈕，就會開始進行刷機啦！

#### Step10

![](https://lh6.googleusercontent.com/MAQk2VAqjJzKauHaH0WJEzeviVk6gXfhtNcL_497k7fdUqRA45HxkBYVa06PhZWskt7eJipw7RUSLtGyYnlZ5eb4uExiFgWarn1GdVMpebWJqNmUdORH8rIeNFlG-qKouwgmadVm)

此時上方會看到刷機的進度，同時手機上，也會出現藍色的進度條，整個過程大約10分鐘左右。

#### Step11

![](https://lh3.googleusercontent.com/ZsfKhzmFWtF0dZlu45iu5bqc3TfivMmMUoAL5Z5mbGO41lTNBM_m4eikcsZKWSxGfxq9WuCT754Iny-L0pWiUgSqawIdsLwu5t0aWcTA5GaN8-UyLCXGygNMfJMYua9JIpkUiuhL)

當面板出現PASS!，就表示己刷機完成，就可將連接線給拆除。

#### Step12

![](https://lh3.googleusercontent.com/KCAA34-rTWf7rLfGYWoM3EsBSwY2xAUgkbjb_LGogaAfFt_Kc6Q94yHHpTRFnRuUeMUZL7vPC8hADORZYI7lKsbdpg0rmQtychbVY2Lr2fNzzxgQoIFf4bGsTNDDPw64LRt90nJH)

這時會卡在SAMSUNG的畫面，別擔心將手機關閉，再執行一次步驟2。

#### Step13

再重新開機後，大約會在SAMSUNG的畫面停個二分鐘左右，接著就會開始安裝Samsung的基本應用程式，裝完後就可順利的進到手機畫面啦！到系統看一下，哈～終於回到4.0.4的版本，這樣就不會再卡、頓、慢啦！

![](https://lh4.googleusercontent.com/Q-fGAalf2rIOdvLYfhM1XzsJGy4gqeWGeozJ2HSrKtuq7c4Sl1H_d-yGSSTl4vP9tiaom9DtYzyaJoo57iEDIZwdu6X-LnqVk1srNEVtUjuxVvpzDoj1vOcLIt9cKU1vI8i_ZN4I)