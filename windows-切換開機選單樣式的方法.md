# windows-切換開機選單樣式的方法
###### tags:`windows` `開機選單` `安全模式`

## 參考
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/1.png)

## 情境說明
1. [開機選單的名稱編輯](/windows-開機選單的名稱編輯.md)

2. **開機選單的樣式切換**

3. [關閉Hyper-V虛擬機的方法](/windows-關閉Hyper-V虛擬機的方法.md)

4. [建立啟用/不啟用Hyper-V的開機模式](/windows-建立啟用或不啟用Hyper-V的開機模式.md)

5. [一次性進入安全模式的方法](/windows-一次性進入安全模式的方法.md)

6. [將安全模式加入開機選單的方法](/windows-將安全模式加入開機選單的方法.md)

## 事前準備
1. 一個擁有系統管理員權限的帳號![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/2.png)

2. 命令提示字元![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/3.png)

3. msconfig 設定、boot.ini 設定、Windows 功能、Windows 進階啟動![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/4.png)

## 步驟

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/22.png)

1. 以系統管理員身份執行命令提示字元，輸入bcdedit以顯示目前的設定

1. 使用下列指令來切換開機選單的樣式 (預設為標準)

切換成傳統樣式: 
`bcdedit /set {default} bootmenupolicy legacy`

切換成標準樣式:
`bcdedit /set {default} bootmenupolicy standard`

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/23.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/24.png)

1. 請關機後再次啟動 (不要直接重新啟動)，使變更生效。

**2017/05/17再次測試，在Windows 10 1703中，把2.3指令中的{default}改成{current}，然後 (直接重新啟動)是可以成功的，所以如果用{default}無效就試試這個吧！**

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/25.png)