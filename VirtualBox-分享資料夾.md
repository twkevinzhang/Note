# VirtualBox-分享資料夾
###### tags:`虛擬機` `VirtualBox` `共用資料夾`
 參考至:
  - http://mh-resource.blogspot.com/2012/02/virtualbox-xp.html

有使用過虛擬電腦的一定知道Oracle VirtualBox這款虛擬機器軟體，VirtualBox能夠安裝多個客戶端作業系統，不過主端作業系統與客戶端作業系統想要互相分享資料該怎麼辦呢?這時就要分享資料夾的功能，此資料夾就像是一個門，連接虛擬電腦與主端電腦，藉由分享資料夾的功能來交換檔案

* 首先，你得先安裝客端額外功能(Guest Addtions)，當開啟虛擬電腦後，點選上方的"裝置"，選擇"安裝Guest Addtions"

![](https://lh4.googleusercontent.com/7LjdGYQ3CUQveyx7GHHKworgw5dzt0-sng0Nl4tHxEVPviCLEMOlkvwQAJJ-cJpOUjaySOQjlQhpe1M8atxiPDRf6edSyBM4or6J9x-Q0Fab1DX-vywLevPVhlaeRHkUD1qlzEPy)

* 安裝完畢後，也是點選上方的"裝置"，選擇"共用資料夾"

![](https://lh4.googleusercontent.com/VGR_39sxZu1RmM-BaBppLv66iAg4gffTUcuFAu6XgrJ5d1H4fo5a4EeOTsCo4l2C6Pkb5_5g1ZKV1R4nfcg68NPDRzgBVI9zm1D5-e8TnVKgGVR5MNzmR9PZM9s81nVIEZkQ9kjX)

* 再按右上角的"加入共用資料夾"

![](https://lh6.googleusercontent.com/Uchw0oAaAxfJcEoPxlbwz6YhrPjjzosvmSSfe6jFNzsXEisKsGBKqceb2FP1gGb9hTEKYAIh0qOsyLh_n4HXIbGAQi1BQhw_jNkB05ynI16gZZ0OyE1Nix-HuPY3qQy_4iKCven_)

* 下拉"資料夾路徑"的選單，點選"其他"

![](https://lh3.googleusercontent.com/s5xPaFXNS1-PQv_jKIRGO4MZ_3IcKQrWKuC4_6ipf19nj1zwptyFfHz5FHUYzpZC8hLYceXpTN-nb4pYsfcK0twKDU-86kkGkNnrBhkgZzW4n-vTTkcwnQZ-cppTLw35olCEPaUo)

* 選擇你要分享的資料夾

![](https://lh3.googleusercontent.com/fK3ys1xwo3yDuBtNij-COTh8PraWm6d-j0ew-JgrqMJFhH-_PpB1sEsLq97bbnWqELDRhjzbWjGb4Lk6i1pCA2CVOH01BScQdMbDOPVcK234sYYCgrV87_39g0fB5WSz4MlvAzK-)

若常常要開啟此資料夾，記得勾選"永久性"，並記住"你的資料夾名稱"，等等要輸入用

![](https://lh3.googleusercontent.com/3xKRU3UEsVFYMTX7pTv9KcAE5V2a7-cfIX0ZpNqD3wGfijPFeRjGTpwf_NJHZuW3OvgooCsVfczVmXLZqLMnBX2u9JqyVqQWStgbKI52XUonGPNkToWXASwbto4VDgrM83vtIUSv)

* 勾選"永久性"的資料夾會被分到"機器資料夾"，反之，則會分類到"瞬變資料夾"

![](https://lh3.googleusercontent.com/UuNkhgNoODR2_45Yd_i1GRhLZEpPMT-vgjM1w8-Cl874XxOY8Tag-PIZrCWOkODAG6jvopjsfNrOLABu-3yXZpvXKzq1c3LHnHwYOM2xVnU9Y_v-pAzVBetfxkxSkTYwh0TD-z-w)

* 但如此還是不能連結資料夾，請在虛擬XP裡開啟"命令提示字元"(視窗鍵+R)，並輸入`net use Z: \\vboxsvr\`輸入你的資料夾名稱

Z可更改成你想要的磁碟名稱，例如:A, B, M, N... 等等，此時就會看到多一個Z槽的網路磁碟

![](https://lh5.googleusercontent.com/9jByx8UPHJfzno3AvvkirK68bfBnqUYtjPqW4lOtGrk-phKn4D6hREZQ7AWIfvfwimoRhXTi6GS9KmT37XlzMe6zKk_RP_08RKHtgfjccKKc1qnoj6gXX3LVBowHmvG_78Ty225l)