# windows-開機選單的名稱編輯
###### tags:`windows` `開機選單` `安全模式`

## 參考
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

## 情境說明
1. **開機選單的名稱編輯**

2. [開機選單的樣式切換](/windows-切換開機選單樣式的方法.md)

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

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/5.png) 

1. 對著我的電腦按右鍵，選擇「內容」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/6.png) 

1. 選擇「進階」標籤，然後選擇「啟動及修復」中的「設定」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/7.png)

1. 再選擇「編輯」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/8.png) 

1. 顯示出boot.ini的內容

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/9.png) 

1. 直接修改WINDOWS=後方的字串

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/10.png)  

1. 按下「檔案」、「儲存」以完成變更，然後重新啟動電腦。

1. 修改結果如下 (只有單一開機模式是不會顯示選單的，這張截圖使用了雙開機模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/11.png) 

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/12.png) 

1. 以系統管理員身份執行命令提示字元

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/13.png) 

**您可以在「開始」、「附屬應用程式」、「命令提示字元」、右鍵「以系統管理員身分執行」(Windows Vista/7)**

**或是對著開始按右鍵「命令提示字元 (系統管理員)」(Windows 8.1/10)**

**也可以「開始畫面」、「所有應用程式」、「命令提示字元」、「以系統管理員身分執行」(Windows 8/8.1)**

1. 輸入bcdedit以顯示所有開機相關的資訊

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/14.png) 

1. 顯示的結果分成「Windows開機管理程式」與「Windows開機載入器」兩部份

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/15.png) 

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/16.png) 

1. 我們先注意「Windows開機載入器」的部份，我們所要修改的目標即是載入器中「description」的部份

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/17.png)  

1. 而「identifier」中所顯示的{current}代表當前正在使用的作業系統；如果您使用多重開機，多個系統中較舊的系統(如Windows XP)，其「identifier」會顯示為{ntldr}

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/18.png) 

1. 而bcdedit用來修改開機顯示名稱的指令為︰

bcdedit /set {identifier} description "你要的名稱"

完成後按下「Enter」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/19.png) 

1. 顯示操作順利完成代表成功，可以再次輸入bcdedit查看或是重新啟動系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/20.png) 

1. 重新啟動顯示如下 (只有單一開機模式是不會顯示選單的，這張截圖使用了雙開機模式，如要在單一開機模式下顯示開機選單，請輸入bcdedit /set {bootmgr} displaybootmenu yes)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/21.png) 
