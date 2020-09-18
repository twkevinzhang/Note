# WindowsRe to USB
###### tags:`WinRe` `WindowsRe to USB` `windows` `windows 7` `USB開機隨身碟`

## 參考
 - [[pixnet] 手動建立 Windows7 x64 USB 開機(救援)隨身碟(Legacy UEFI)](http://iammic.pixnet.net/blog/post/65789494-手動建立-windows7-x64-usb-開機%28救援%29隨身碟%28legacy)
  - [[edu] 將 install.esd 轉換成 install.wim](http://blog.ilc.edu.tw/blog/index.php?op=printView&articleId=488747&blogId=25793)

## 事前準備
 - 建置前需要準備 Windows 7 x64 安裝光碟與 USB 隨身碟

## 認識與注意: 
 - 以下以windows7 x64為例，實測windows10也可以使用
 - 使用 Windows 7 x64建置完成的 USB 隨身碟不支援 32 位元程式，如果需要執行 32 位元程式，需使用 Windows 7 32位元安裝光碟進行建置。

## 步驟
### 執行 diskpart

1.  使用管理者權限開啟命令提示字元。
2.  輸入 `diskpart` 指令。

### 清空 USB 隨身碟 (隨身碟為磁碟 2 7400MB)

1.  輸入 `list disk` 查看磁碟
2.  輸入 `select disk 2` 選擇磁碟 2
3.  輸入 `clean` 清除隨身碟

![](https://lh6.googleusercontent.com/Ut5s9N3mULsGLhIqI_3e-VJrwYPRnAflOWOQ67CdErApqmUgRLbQ_d8TvbjM722OVntHQXdnxrayIUDSa_1HuBjSMbgV9P56F8deVCkXToaOSpZQonu6olU4GH8V5T1sFB05cH1R)

### 建立 partition 與 format

1.  輸入 `create partition primary` 建立
2.  輸入 `format fs=fat32 quick` 將隨身碟 format 為 fat32 格式



![](https://lh4.googleusercontent.com/X5eIZYExS8PR7HVw7nGSmogfkxjE_n9imkTDWBRHo9kfbHkG3gFbiw3-prVXxbf0qqb5ThJLAb_kZpwVbyDZil9KA2F_Hq9-hQ6O2WDbQcTOU2SLI-9YZ8czWMWCntCrdHVJAMw1)

### 設定 Partition ative

1.  輸入 select partition 1 選擇分割區 1
2.  輸入 active 設定該分割區為 active


![](https://lh5.googleusercontent.com/PeF-5wDuaCLWgDfKR82dI6h9A6fea9upYHm78iuPcgEUaRbBLK9KRU-JpLgu68TnSUPIfObDB0GUKRetSAxHcJXB3tyB3ByUroxGVH84KQ-GMnpnuoGssxxCCekxLW3BGJB7Ndey)

### 設定 USB Boot

1.  輸入 `exit` 離開 diskpart，之後將Windows 7 光碟放進光碟機 。(目前本機中的光碟機位於 D 槽)
2.  輸入 `D:` 跳到光碟機。
3. 輸入`cd boot` 進入到 boot 目錄。
4. 輸入` bootsect /nt60 e:` 建立開機程式到 E 槽中。


![](https://lh3.googleusercontent.com/2XR9WxMAflRcfE6qjmC2WmgpVRwilkbzXi5CIWaYXOoH0_SLCF2gXk5JXcObIRiK7i_M8brGP-HrshWq1Noaymiu601s2rrgEpN-naKhtqKB2oMMpmQWH3NUnxvUrAH1yUzfGA5-)



1.  輸入 `xcopy d:\boot /s /e /f e:\boot`後輸入 `D `( 將 boot 目錄 copy 到隨身碟 )
2.  輸入 `xcopy d:\efi /s /e /f e:\efi`後輸入 `D` ( 將 efi 目錄 copy 到隨身碟 )
3.  輸入 `copy bootmgr* e:\` ( 將 bootmgr 與 bootmgr.efi 兩個檔案 copy 到隨身碟 )

### 擷取 WinRE.wim

1.  輸入 `mkdir c:\test`在 C 槽中建立 test 目錄
2.  輸入 `copy d:\sources\install.wim c:\` 將Windows 安裝光碟中的 Install.wim 檔案 copy 到 c槽。

如果沒有install.wim:

 - http://blog.ilc.edu.tw/blog/index.php?op=printView&articleId=488747&blogId=25793
 - https://drive.google.com/open?id=1GeEdyGkHVpz9dqpZKgGdpqlooe2LknbTFS4FRZpGCHY

3.  輸入 `dism /mount-wim /wimfile:c:\install.wim /index:1 /mountdir:c:\test`  將 install.wim mount 到 c:\test 目錄



![](https://lh4.googleusercontent.com/MtRAzhYsgzcb4pv2edHpGbvYJL-eCX4gORz2Bb7jmvA2D-8Bab1g1dw4oy7AoG871M1PXQRfmILeZsgB9X-hmtTjq3hUT0gg7achetZ7LiI5BAUH_Ttnw0kdWOud5hy3VrvHp6i6)



4.  輸入 `copy c:\test\Windows\System32\Recovery\winRE.wim e:\ `將 Winre.wim Copy 到隨身碟
5.  輸入 `xcopy c:\test\Windows\Boot\EFI\bootmgfw.efi e:\efi\boot\bootx64.efi` 後輸入 `F`(將 bootmgfw.efi 檔案 copy 到隨身碟中的 `/efi/boot/bootx64.efi`)
6.  輸入 `dism /unmount-wim /mountdir:c:\test /discard` 將 install.wim 檔案 unmount



![](https://lh3.googleusercontent.com/SiSEwrjdfplIy_rOlKhLdH_sumWtxH1PXHOlKjV-4kphg94twEZ9RbpOo2LzDAdVFpicWy_whPfaxUPUso8qNYCPl4rj_bCsY1Fa-voW-u2ihtXu5xpzaReRCPNVzGCWjtlYEV4t)

### 設定 BCD (Legacy Boot)

1.  開啟 Bootice 程式，選擇 BCD 編輯頁籤 -> 其他BCD檔案 -> 選擇 e:\boot\bcd後點選高級編輯模式。可到以下網址下載:

 - https://sites.google.com/site/gbrtools/home/software/bootice-portable/bootice-downloads
 - https://drive.google.com/open?id=15k_GShK8hFW7uWxlzixaXhw593S0c6s2

![](https://lh4.googleusercontent.com/oKfwMKl7DOoNQHC9UNjVrItj-pxRc3I_UEX3Vv6FXEDbpvBlev8l-vt92EOCghyfSDdq13y-bIIbUZIQxhR4NS0kxBYKjh_MHxCXjTvHWA8W6ETq_r94f2QXbRLObl6ood-JgirM)



2.  修改 ApplicationDevice 與 OSDevice 中的 boot wim 檔案

![](https://lh3.googleusercontent.com/mAMmVbVYHj671Ina5CM-qVa7MDjrpiE0b30UDenTs3GLevLyvebco7NY1IqBbKT8kerDpm5knj-9c3nb2lXKyo6kNEX_WHL3MbTG_jEngvKIWSz7QVbwDEBvvouLdPA5zP4GuI2z)

![](https://lh4.googleusercontent.com/xu6lTpcfiNV64SRNx9NJCDzjidSSltHq17TuGtaHA0Nemm3gjZi3DyoAgy9UXR21s_FlD4IiExd3QjIPLM7ui4Y61vKQACcP_M64XoPxB5ON4o868KDPfFVUuGU_s07a5x8GN502)

### (UEFI Boot)

1.  開啟 Bootice 程式，選擇 BCD 編輯頁籤 -> 其他BCD檔案 -> 選擇 `e:\efi\microsoft\boot\bcd`後點選高級編輯模式。

![](https://lh6.googleusercontent.com/cDHPnA40aV4999ufjseNmVuB-5yQn4Xrd2nHOvkQNC6BOQ7wYsg8CNlIVR2ujkKDb6nU06xX1TPNluzVUwkvXNjPwmG_95_kLHNXGQ4zVTSox9XYkN9DczZ5CyonIaX_NtvPZa4e)

2.  修改 ApplicationDevice 與 OSDevice 中的 boot wim 檔案

![](https://lh4.googleusercontent.com/T365XkijxK793L1L_PM_OPD-TEwWMsSawR-yYYGeiqAhzv2nVqqq5t8xewlD24KdS2SXflkiInhUqkfqgfNtTC_WwKRWfD9AIZeD9XnvlliJfAUmGYCHES-xJ6hg369ydhuRdbbG)



![](https://lh3.googleusercontent.com/Asmday1bczUdI7TYrKeK8y27UWyXIA4azCLvujRZ_MZlUrdwnpivV3QuICvslnFru-0gq9p-i05_BAkLUIz4nxBxFrj8brHRvoCKYCcQ250WXX4UDXJ0i_Rpbd6Lqed7JuAjfiCm)

### USB 隨身碟開機

之後使用 USB 隨身碟開機，就可以進入 Winre

![](https://lh4.googleusercontent.com/lcc0mNOEeH44e1W6EshYdfTWgg3ahj1VIq6qxjzWmw9s2gyiG1bzjdLrgqUPxzNlMoSHR2bxgKO5LYUsrnArb0fG_afReoTiOJtFLoiJJ9Orz5l6VA970omxYf_dtulXHi-hcrQN)

![](https://lh4.googleusercontent.com/pL4QqaWYWMznJvazXLoc2kSxCGCQ0b4oYX52RBjQvFXaWA4aC6gH1xmF3LaEV5JYFgI0Ps-0XPmDzCgkInDWDbfKQ4_ETOmZJcivuwHoqcR_XWFRbqc7huTVMG4UoH5IyCanaEqc)

![](https://lh5.googleusercontent.com/XoQZVl2VU9EmxltXWdGRiwGx39GaG1N9trlcZM9yLT-Wgvxm6knLb_WFVxE07mwOdlkI-USsA3G4RgPaNoe3syxzNaAyRrPbZ9XONOVXpUtIP46uSbLgnE2VtsG4mxElr_RLA1my)



![](https://lh4.googleusercontent.com/ygXgUH-nfkkZuCnjziG9vQndXlbcjtyj9cMmFdLkADC5mQWhLgPC-ChbZ2fLYva8OniTm9E9YDxgn4-s92QJVcFfzhk7CzHc-RAy5r5aGNmJkA-IAceGKQOezPrw5DZ__7_l8epd)

### USB 隨身碟開機後自動啟動命令提示字元

Winre 開機後會檢查 Windows 版本，來決定是否進入 Winre 系統，這裡將把這個檢測動作關閉，並自動開啟命令提示字元。



1.  輸入 `dism /mount-wim /wimfile:e:\winre.wim /index:1 /mountdir:c:\test`  將 `winre.wim mount` 到 `c:\test` 目錄
2.  輸入 `attrib –r c:\test\Windows\System32\winpeshl.ini` 取消檔案唯讀
3.  輸入 `notepad c:\test\Windows\System32\winpeshl.ini`

![](https://lh6.googleusercontent.com/pM5hSwN2lMRlSiuM86VJREsDQ9KmQlyvmxh7oF4E0Clf0lPk5boVfyr2A9Zg4dy6a0Xxuvlp_8GlVKfXxLN_deEzMUDaxWD6qx3FbkkqfpGfcwxgYfQpy9x2s5pqPgizhWl06YiX)

4.  將下方 AppPath 路徑改為 cmd.exe 路徑
更改前: 

    [LaunchApp]

    AppPath=X:\sources\recovery\recenv.exe

更改後: 
    [LaunchApp]

    AppPath=X:\Windows\System32\cmd.exe

5.  輸入 `dism /unmount-wim /mountdir:c:\test /commit` 將 winre.wim 檔案 unmount



![](https://lh5.googleusercontent.com/cB4k29VgDyj2xOUhxCu0EO7Q9VkfP4jMiZx8MDvM-gGPGZ6S6j_jEZK95our9YGdIrXeoTB3AH4-twtyUVOMsxOLWDlPIE-QwEVTfHmSRnmmsWGA1IjHBCLdrADSoT26MfWN5eO-)



USB 隨身碟開機後畫面



![](https://lh6.googleusercontent.com/b-wfdiwiSc2v0-lI_OLcmZVWq803HL9Hvg4EfXjBeM02nK_mnNB7LS8KjQbZ9-B5fVhlyRdgONrUSHsTU76GD6KA0SnaDWThkUWgHkC1-b-duKsYz1ZhLQcK4cnzss8q43ihM3tc)