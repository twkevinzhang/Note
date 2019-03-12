# Win7-更新後無法開機，該怎麼辦?
###### tags: `更新` `開機` `error` 
#### 第一招：安全模式

正常模式進不了桌面那我們就先試一下安全模式，要進安全模式請在開機的時候按住 ［F8］ ，系統就會出現這個「進階開機選項」：![](https://lh6.googleusercontent.com/6gkIHiMcjbr6lYRMM2-h6maJtXVDwa2UiafzVSK1Iqpah8q9F82pk6MrJ9cl1usmVX8Pf8Y2ll0GrLA7Q_ycEnKNjSdq2cEZfWbA7yfZ3bURUGgcJdLgvvyDHJ7lyIhzlrm03Rol)

註：華碩主機板按 [F8] 會先出現另一個開機裝置的選單，請看選取硬碟開機，然後馬上再按下 [F8] 才會出現這個開機選單，記得「馬上」哦!請選擇後面什麼都沒有的［安全模式］，有時候進安全模式什麼都不用作，再重開機電腦就正常了！

但是這一次是因為自動更新出問題，所以會出現這個「設定 Windows 更新失敗，正在還原變更」的訊息，之後再重新開機 - 還是進不去！![](https://lh5.googleusercontent.com/vyiRCWic9yqmXCzecIm4ZXODhNHARHckX4MgdQoBPH9YvqxQF1Tpol8LcLIvMADiWvrMH_ImuBPbgmwSiSlypF1RJNvlc14Om9JGFuq4aYfLrYlBkF0b8j0Ih8h4tUZdemQ3RBW2)

還有另一個選項就是［上次的正確設定（進階）］或許也可以起死回生，但是這一次還是不行 !

#### 第二招：啟動修復

接下來就要手動來修復硬碟的開機磁區，請一樣在開機時按 [F8] 叫出上述的開機選單，然後選第一個［修復您的電腦］接下來的「鍵盤輸入法」直接［下一步］![](https://lh3.googleusercontent.com/dp4dS7FY7kNlix8Zr88OMek9s9w0p3SM18t4c9aNHW64u5KKxeccz0tEf0wSgWxdW8uCJJpo88aqISeQ85PjmH9l8aDbaKkxkQtXEMm9qgE7P3psIDSVv_rdrSGb6iysF5EYXj1q)

然後選取一個有管理員權限的使用者並輸入密碼

![](https://lh3.googleusercontent.com/GqCsc7Q-2oljzdTng0QqUZZJpLASjAuvNA7s2Bxu2Mx6c02NiiQAsW3tCzgnh_NQbp3OLvquKGJavVsqHqulKUknKRiPf5L2OhiF8TNi3PIn2jX9OZBICBZ2y_HDTsJJnTp_1uZL)

如果無法進到這個「系統復原選項」的畫面，那你的電腦開機功能應該已經毀了，請改用下面的光碟開機法來執行修復，還是有可能起死回生的！請選擇第一項［啟動修復］開始修復![](https://lh4.googleusercontent.com/XpHu41czpCiZ4iWRTGMujUBYksEznuLIesI85c8zLXYVKW3dRu3lWan9-qpyB3Q11SGN3mREh2UIO2xo1emYifhXnwXVD7-lbIawP9cC_VLIg5FEx8X60FBCP5gsAm9HUTCooIW2)

這一次因為不是啟動磁區的問題，所以沒有找到問題，如果你的啟動磁區有問題或許這樣子就可以開機了

![](https://lh5.googleusercontent.com/nkqUfIY2zPLHNBZ8iCf3k1ZvxKn2gKAKHLhED2uaQfbPYsuf4_KzmuzmvuOkclDYmGtcPOY2u1EyCtZ_U2uL2Zf8gNedNEWXXGc3fke4V6i3Z6d0zmKkRfeJODR7_YIQ3X98XeET)

#### 第三招：系統還原

再不行就要將系統還原到出問題之前的時間點，但是如果你已經把系統還原關閉了，這這一招就不靈了請在上述的「系統復原選項」選取第二項［系統還原］然後按［一下步］![](https://lh5.googleusercontent.com/VjMycRA16Xj6SikLds3vINX1vowOxI_AvFScEkO50yC027r-Xsxz7wOutoPZUeMmMsIs0eqhIxxdv0C7dvsbsPUwZl3uWvAfU6JfclXOIPUpJv_-8HohCVON9cNOb-itp-6qUQJD)

再選擇要還原的時間點，如果太少還可以勾選「顯示更多還原點」，再按［一下步］![](https://lh6.googleusercontent.com/lfbZ3t_5IBGhxRjW_GMevjOruNPucmu7m_7hXM11BrFQCjmXfzfsldnrPrtiDt6V_DhCiRWQ3De-dTqGxbOcpFP1T1hjQ-5NXFhoayupt2QWsUeruJnBCrTjI_gWTZe-Gybqx48H)

在確認的畫面按［完成］開始還原![](https://lh5.googleusercontent.com/5y2Gjkqldl2ULT294ag0qswkitJIFK0y4pDB-0wxFtpmjGrJZUHmsULmL_D562fJihQakdht0OswLOcm5MWKYBvnGdJlOYMRd74i9yHXyD-UXfuRwp8fm6QEqq2d4bt8dgASBekW)

最後一次後悔的機會，確定要還原的話按下［是］![](https://lh3.googleusercontent.com/_vyxcQ-GkaNpC-q025NSStdjmWV-GXNYitbj4HVtTgkIsh0F9awCgGGNrvuK9zoWSWkRHzmo1D-nSFat4e4UrGX_caz609L9FipzuwAnY66iKN8XejHhoB3_0a81QOmHtSwJT-t5)

終於成功進入桌面的，這是告訴你已經還原到哪一個時間點![](https://lh3.googleusercontent.com/N1Qd8mdvchsAm0Fj_50KSYZ7ngaIkibj7FP9Ge99PpbevQBxozQ-FWmt9tUCT3q_1vF8F3FzDR2tcqgnsJe1gYH-_EElKZIpg-wzjzibB1qSyGSXB_6IpXArBfCD8LPoxwHR0Fu9)

還原成功按［重新啟動］重開機![](https://lh4.googleusercontent.com/YipazornDxF16oEkFl6ca-wzSUdtxEV6wX0CniyaswwybtaYG7Prln9mPsgbcDyF0zElljijM9FPq9kRe28qyNZizHN0J4_nddMJG6CIR8XbyxUy2lX3HmQfHbgyX11i9WNpxSqj)

使用原版光碟開機修復更糟的狀況就要找出Windows7的原版光碟來開機了，記得開機要選擇由光碟開機，然後在螢幕出現「Press any key to boot from CD or DVD」時按下鍵盤任一按鍵才會由光碟開機以下是各廠牌電腦／主機板的開機熱鍵華碩：主機板【F8】，筆電可能是【ESC】技嘉、Acer：【F12】微星：【F11】這是光碟開機的第一個畫面，直接按［下一步］

![](https://lh5.googleusercontent.com/efro8k8cLJV0P7IXcrTJa2JwPHK800s3iTiY_y_VqCAlJBRBZkSBB_yMxEO69uB2wGBPjdNXmMvAeY_mFc3D0LU5_20hAD3fDqoSB1vSIfGwL95THtE1xodgnWLGgXUcEIXCXJFW)

在這裡選擇［修復您的電腦］

![](https://lh5.googleusercontent.com/B8-RilmxTsuk0-terr0qe7iLTPqzSzauOhl3oip3OZPGSVdlou14qbnyR56WAlTUXeub5aJJrT5Ct0q-c82b6xYCwet-qpeJmAwf2-8vXOw6Y3zDL-b9fIy7ODgnMmLhrv7-jIxR)

系統會找到你的Windows7安裝位置，按［下一步］

（如果你仔細一點會看到磁碟機的代號跟你原來的不一樣，那是因為你的 Windows7 在硬碟的最前面有一個100MB的特別開機磁區所致，這不會讓你的磁碟代號亂掉的，不用擔心）![](https://lh6.googleusercontent.com/5WzLHwqx6mxJjmqgjB1feTzJW3M9K1YAKdK2QhdLTXQV9qYmuXJe1I2oYP6JydeSyn1HGtkeQ-e68DuNFyh7HlDjidqtZDBcuIla_tKHGbc_OvWrD-Qpk3cJGK_ehTMF5L8ddwqr)

接下來的「系統復原選項」跟前面由硬碟開機的都一樣，你一樣可以執行［啟動修復］或是［系統還原］，甚至是［系統映像修復］![](https://lh5.googleusercontent.com/JvUZuL-HWDLk3Gq3JW_m326Yvp7izzf148pQvKu5EylYPyki6iHiHL8LHndpPJBoaoDs1HcNQUZfm7bSKq7HQp7HrvSKICiRCpAPbyUHNOExkd7pyrzuU3HI706iPg41V8-RmcvJ)

真正出問題的是 pending.xml以上的方法只是教你還原，但是真正的問題還沒解決呢！

原來系統會卡在「正在準備設定 Windows，請勿關閉電腦。」是因為更新完之後可能會有第二階段甚至第三階段的工作要執行

而出問題的點就是在執行第三階段的時候出問題而這個第三階段就是利用系統開機時自動執行一個 penging.xml 的腳本檔來完成的，現在更新完卡住了我們只要將這個 pending.xml 手動刪除系統就正常了

方法如下：不管是硬碟或是光碟開機，請選「系統復原選項」最後面的［命令提示字元］，另外你還要記住我特別框起來的磁碟機代號，這裡的例子是［D:］![](https://lh3.googleusercontent.com/8ay_biD3mUqloEgt1vaZEPu5LbWJlzhHZZdIpEXMUgAvPslYNa2hXRUsK4CkZEwOUs65b7MYNHYhX3-HZlcGOXdXEhUEJKEPN-UchwIVznA-oxvi9khOSCC4xQlDo5SVolrQGBMf)

然後在命令提示字元輸入以下的指令：

cd /d d:\windows\winsxs dir *.xml

（如果你的磁碟機代號如果是 C: 的話，第一行指令請改為 cd /d c:\windows\winsxs）

del pending.xml

是不是有看到兩個 xml ？接下來再下指令將 pending.xml 刪除

然後再重開機就大功告成了！