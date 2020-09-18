# windows-關閉Hyper-V虛擬機的方法
###### tags:`windows` `開機選單` `安全模式`

## 參考
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/1.png)

## 情境說明
1. [開機選單的名稱編輯](/windows-開機選單的名稱編輯.md)

2. [開機選單的樣式切換](/windows-切換開機選單樣式的方法.md)

3. **關閉Hyper-V虛擬機的方法**

4. [建立啟用/不啟用Hyper-V的開機模式](/windows-建立啟用或不啟用Hyper-V的開機模式.md)

5. [一次性進入安全模式的方法](/windows-一次性進入安全模式的方法.md)

6. [將安全模式加入開機選單的方法](/windows-將安全模式加入開機選單的方法.md)

## 事前準備
1. 一個擁有系統管理員權限的帳號![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/2.png)

2. 命令提示字元![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/3.png)

3. msconfig 設定、boot.ini 設定、Windows 功能、Windows 進階啟動![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/4.png)

## 步驟

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/25.png)

1. 請進到「控制台」、「程式集」，選擇「開啟或關閉Windows功能」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/26.png)

1. 查看Hyper-V有沒有打勾，如果您不需要這項功能，可以把它勾掉

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/27.png)

1. 您也可以透過bcdedit指令來查看Hyper-V是否有啟用 (見結果中的hypervisorlaunchtype)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/28.png)
