# windows-一次性進入安全模式的方法
###### tags:`windows` `開機選單` `安全模式`

## 參考
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/1.png)

## 情境說明
1. [開機選單的名稱編輯](/windows-開機選單的名稱編輯.md)

2. [開機選單的樣式切換](/windows-切換開機選單樣式的方法.md)

3. [關閉Hyper-V虛擬機的方法](/windows-關閉Hyper-V虛擬機的方法.md)

4. [建立啟用/不啟用Hyper-V的開機模式](/windows-建立啟用或不啟用Hyper-V的開機模式.md)

5. **一次性進入安全模式的方法**

6. [將安全模式加入開機選單的方法](/windows-將安全模式加入開機選單的方法.md)

## 事前準備
1. 一個擁有系統管理員權限的帳號![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/2.png)

2. 命令提示字元![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/3.png)

3. msconfig 設定、boot.ini 設定、Windows 功能、Windows 進階啟動![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/4.png)

## 步驟

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/33.png)

1. 先找到「進階啟動」，再按下「立即重新啟動」

您可以由「常用工具列」、「設定」、「變更電腦設定」找到「進階啟動」 ( Windows 8/8.1)

或是由「設定」、「更新與安全性」、「復原」找到「進階啟動」(Windows 10)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/34.png) 

1. 出現「請稍後」畫面

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/35.png)

1. 出現可供選擇的選項，這裡請選「疑難排解」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/36.png)

1. 然後選擇「進階選項」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/37.png)

1. 再選擇「啟動設定」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/38.png)

**正式版應不會有「回復至先前的組建」這一選項**

1. 按下「重新啟動」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/39.png)

1. 重新啟動後出現選項，在此筆者選擇F4(安全模式)作為示範

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/40.png)

1. 成功進入安全模式

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/41.png)

1. 不過下次開機將回到正常模式，除非您變更預設的開機模式。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/42.png)
