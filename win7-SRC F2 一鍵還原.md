# win7-SRC F2 一鍵還原
###### tags: `重灌準備` `windows` `win7` `SRC`
 參考至:[https://iblog.ph-wbc.com/windows-7-src-f2/](https://iblog.ph-wbc.com/windows-7-src-f2/)

(未嘗試)

#### 開始

首先要準備以下東西：

1.  windows 7 安裝光碟 or 安裝隨身碟 。

2.  XPE工具… 通用 PE工具 (分割磁區用) 。下載點：http://www.tongyongpe.com/

3.  SRC F2 一鍵還原工具。下載點：[https://mega.nz/#!XsZhgYgR!Vo1xYAxHmGdFs5iaUEuxJsS_xktuYG6FFKs62rQRdOY](https://mega.nz/#!XsZhgYgR!Vo1xYAxHmGdFs5iaUEuxJsS_xktuYG6FFKs62rQRdOY)

#### 分割磁碟

一開始使用XPE工具開機，進入XPE系統後，選擇分割磁碟

此範例為一顆全新的硬碟進行分割，所以無任何磁區在上面



因為硬碟是 500G .. 把 100G 分割給 C 。如下圖…

並先不用格式化!!等系統安裝在格式化即可，也等安裝完系統再來進行分割其他磁區

![Windows 7 SRC F2 一鍵還原](https://lh6.googleusercontent.com/Gr-QwJPdvW4iS216WBlpNbNXh4vGqy6hLsZzhmXkfaI8VIMmWTsJ9aW7Qd5P8NYjhTd0RCMFG8Z2mzYpu4K9vSSZ3jTSpDel7WRPGyj4dYFfRmAW24MRoovBiYLcvn90AE1w9U14 "Windows 7 SRC F2 一鍵還原")

完成分割以後，就保存分割，並離開分割程式…開始進行 windows 7 系統安裝

#### win7安裝

使用 windows 7 系統安裝時，會看到只有一個磁區



並格式化 100G 的磁碟區…然後進行 windows 7 系統安裝，直到安裝結束。

![Windows 7 SRC F2 一鍵還原](https://lh5.googleusercontent.com/enh2f8ROTXKGmk8KLvqqYwygXC4V5oPLU2ioIW2Qcvb5T1Nj2bGRiQh-cIWITLImt5hq6Xm1HQgVRGwkZ9qHnPIpNst__zaUwUPuPpq1TpdmpbknghgSN_7CoqqbqaPkmLDx_Ixh "Windows 7 SRC F2 一鍵還原")

格式化結束，並安裝完系統以後…就可以開始進行驅動程式及相關程式的安裝

我主要會做的是安裝驅動，日常程式，系統更新…做完以上事情才開始進行還原設定因為這樣只要還原以後，就不用怕沒有軟體，系統尚未更新及無驅動程式…

#### 開始分割SRC還原空間

當前置作業做完時，這時候可以來開始分割其他磁區了..



我打算分給 SRC 還原空間 20G就好，剩下的就在分割為一個磁區..

SRC 的磁區，必須是要 FAT32 格式，而且一定要是主要磁碟分割

會打算分 20G 是因為我有做過測試，20G 拿來放還原資料還有剩…

如下圖，而 SRC一鍵還原的作用是 把 1:1 的資料備份到 1:2 的磁區

然後 1:2 的磁區就會隱藏，避免資料遺失…

![Windows 7 SRC F2 一鍵還原](https://lh5.googleusercontent.com/LVT0TXNz7nNsq3H6gI2QRokwsRa0puveJVaF38JdKh5OUYMQMA8mvJfTRLrRFKypli_hA8KoqNLdpRlfEN504_MkjnigytBEfDREEp_6OzKsqrbrBl6_QqPUCQWiSGbbIB6TdvJQ "Windows 7 SRC F2 一鍵還原")

當都完成以上步驟，就可以開始進行安裝作業…

把下載下來的 SRC一鍵還原 檔案解壓縮，然後進入 src 資料夾找到 SRCLIENT

並把 SRCLIENT 設定為以系統管理員的身分執行此程式 ，這樣才能成功寫入

![Windows 7 SRC F2 一鍵還原](https://lh5.googleusercontent.com/ME_ne_sSUWYbrXq1cB_M1i7SxIEwTV8vJTo5XyIkkmj-isq32Q-q65WSe24shP6acSPdNKMmmyhKc2LHz5TyXLW4skC-1S426yG_-Udd8_hE901tnyok945rlwGb9mYg5CXqnTLX "Windows 7 SRC F2 一鍵還原")

接下來回到上一層，就可以點選安裝進行安裝 src 動作

點選安裝之後，會跑出一個小視窗，等他跑完會出現以下視窗….

這時，剛剛分割好的磁碟D就會被隱藏起來，消失了 !!

![Windows 7 SRC F2 一鍵還原](https://lh4.googleusercontent.com/w4ALXWbcaYseP84cMAia80veeAWzrtU-92XLvTFfZu6sdmaovMuDtygnp0YOqIUIxFwhJjstP93mgskxP_b56-_Wob3ZhoXQTOpIaFjQYLOHEfI77luAtHeAlwFAFZECygENQeH6 "Windows 7 SRC F2 一鍵還原")

點選還原硬碟的MBR，可以把消失的D槽叫回來，也有些小設定要做變更

![Windows 7 SRC F2 一鍵還原](https://lh6.googleusercontent.com/kejdnmMdEbSeYVmA2cqr5_vAirj5W1OQaAWCMqT7-xsXq318-Rj1Y7Ek0dJTSO7LIkX6a7jbkUB1kBR5qkn0GyqFwzuqbDWPinPAr1Nz8HZ7kIZHD0ftqYqJYLnxc2eT1YYzO8_O "Windows 7 SRC F2 一鍵還原")

點選 YES，就會通知說 MBR 已經回復了，去看D槽也出現了

![Windows 7 SRC F2 一鍵還原](https://lh3.googleusercontent.com/SsJGblY_bzY13NRBjygt2sea0IninfjRTlbD4Sqj4XiCl2bo2-t91rSPAE39CTAStOvvJw5eTfl15ymOP5vWHFWKt76_P9PORoZMOhPAAJDs-CQy_y3DhSlwvdcYux9xPG9Qf4W9 "Windows 7 SRC F2 一鍵還原")

接下來可以直接關閉視窗，或者是進入 其他選擇 ，點選 DOS 離開

就會看到 D槽 名稱變更為 SRC，這樣就是有安裝成功 !!

![Windows 7 SRC F2 一鍵還原](https://lh6.googleusercontent.com/8ofL6UyyiRwczwxTQMs9SwSWoWi56YcNORLa7OjWpYeqGMcTtEwjoppaT4HZ-Dn6R4c79yZMRXEWBNuRq2M0MhhZb3VZ47e5YpdXqixw6S-LeJ-5aG4hW8IfBvrMjMaqm61PR6gJ "Windows 7 SRC F2 一鍵還原")

點選 SRC 進去後的 src 資料夾找 SRCLIENT ，並用記事本打開他!!

找到以下字串，此地方的 54.6 = 3 秒，因為一秒為 18.2，這是電腦開機顯示 F2: 的時間

![Windows 7 SRC F2 一鍵還原](https://lh5.googleusercontent.com/JGnr8y0uQa4kUu1WnVEmfaTymVqVSdDy9ZeFsqvHyFU0WfqX5xOFBN_wzHEy-uBv1IkW29drRy6STemRnAI3ykPxd_g8F-TqXk2JAd0LZ1PeBo_k1TqgaW-atFF8SQwnvD-TBN7w "Windows 7 SRC F2 一鍵還原")

為了要顯示久一點，不會錯過按F2的機會，所以我改成182，也就是10秒

![Windows 7 SRC F2 一鍵還原](https://lh4.googleusercontent.com/krRzoC23FDuomAM9rWcJ8ypNXdQCO75aQbfCXY_uiDyXDycyXLSRvG_y2Au5EXYrS3Zh6csx-GPc9mg_nqDL1SEbPi4F83yBrJFn1MQng12ooGdGLRj99-kAjRQfWtvz_SDmoq4Z "Windows 7 SRC F2 一鍵還原")

接下來框起來的地方，就是指定按鍵的地方…我都用預設值，或者是可以自己更改

“F2:” 這個為顯示的名稱。value=”60″ 為對應編號。 F2 = 60 .. 依此類推 F8 = 66



設定好以後，就存檔關閉，重新開機，就可以開始進行備份工作

重開機後，螢幕左上角就會顯示 F2: ，此時趕緊按下鍵盤上的 F2

![Windows 7 SRC F2 一鍵還原](https://lh3.googleusercontent.com/t5yG8dsXeXFoanOYy7Z-CNE3oyXLenvh7vr9VABr9eMn60Upu3HjAr37N1IKhJes3t8c5qDmz1NyYPTz1ZohbVfN0gECgCuiKMn1wJ3rAMMEvxq5Mb7zBebC8Fk2N4vKO-bXeCQV "Windows 7 SRC F2 一鍵還原")

按下 F2 以後，就會跳出以下畫面，表示有成功



再來，點選其他選擇，點選DOS離開畫面



離開畫面以後，會跳出以下字串 C:\> ，有玩過 win98 的人應該是不陌生…



有 copy1 、copy2、copy3 可以用，但是用 copy2 就好了

此時就打上 copy2 ，按下確定

就會顯示 Press any key to continue… ，意思就是隨便按一顆按鍵進入備份作業

就按下鍵盤上的任何一顆按鍵吧

![Windows 7 SRC F2 一鍵還原](https://lh5.googleusercontent.com/8C_s_2t2-1Pql57qDX--FpletqwezCYZ7yE5X0-itSH3KFzPEXidmkSBNY5I1dQ_zgkhi2Ai4Uq-9--97hORzfKMEGKoJ93bLczasa2LW2bEM-UvYPnLj5ULBEI2ZJ1Fan4CUgbQ "Windows 7 SRC F2 一鍵還原")

接下來就會顯示以下畫面，就表示開始備份了…備份完以後就會自動重新開機



以上是製作備份過程，如果要還原電腦的話…

開機後，顯示F2: 時按下 F2 .. 點選底下的還原我的電腦系統，就會開始進行還原了 !!

注意事項：SRC 磁區可以在第一個步驟就分割，但要是 FAT32格式，而且要是主要磁區…不然會無法使用

其他可參考:

# [作業系統][分享]Windows7 x64萬用還原(完全@9.42G@MG@繁中)

[http://www49.eyny.com/forum.php?mod=viewthread&tid=10546776&highlight=windows7](http://www49.eyny.com/forum.php?mod=viewthread&tid=10546776&highlight=windows7)