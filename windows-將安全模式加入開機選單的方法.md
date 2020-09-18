# windows-將安全模式加入開機選單的方法
###### tags:`windows` `開機選單` `安全模式`

## 參考
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/1.png)

## 情境說明
1. [開機選單的名稱編輯](/windows-開機選單的名稱編輯.md)

2. [開機選單的樣式切換](/windows-切換開機選單樣式的方法.md)

3. [關閉Hyper-V虛擬機的方法](/windows-關閉Hyper-V虛擬機的方法.md)

4. [建立啟用/不啟用Hyper-V的開機模式](/windows-建立啟用或不啟用Hyper-V的開機模式.md)

5. [一次性進入安全模式的方法](/windows-一次性進入安全模式的方法.md)

6. **將安全模式加入開機選單的方法**

## 事前準備
1. 一個擁有系統管理員權限的帳號![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/2.png)

2. 命令提示字元![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/3.png)

3. msconfig 設定、boot.ini 設定、Windows 功能、Windows 進階啟動![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/4.png)


## 操作

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/43.png)

1. 以相同的方式進入boot.ini的編輯畫面

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/44.png)

1. 換一行加入新的開機模式，內容的格式為

`multi(0)disk(0)rdisk(0)partition(1)WINDOWS=" 你能分辨的開機名稱" /fastdetect /參數`

上述的內容請根據您電腦的情況進行修改

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/45.png)

1. 再換一行加入新的開機模式

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/46.png)

1. 重複動作至您所需要的開機模式全部建立完畢為止，存檔後重新啟動電腦即可。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/47.png) 

1. 完成的狀態如下

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/48.png)

1. 嘗試進入安全模式。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/49.png)

1. 成功進入安全模式下的桌面。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/50.png)

1. boot.ini中可使用的參數如下︰

 - 安全模式
 - 安全模式含網路
 - 安全模式含命令提示字元
 - 啟用開機記錄檔
 - 啟用VGA模式
 - 目錄服務還原模式(僅限網域控制站)
 - 偵錯模式

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/51.png)

1. 以系統管理員身份執行命令提示字元，輸入bcdedit以顯示目前的設定

1. 為了增加一個開機模式，需要先利用指令把現有的開機模式複製一份再進行修改

該指令為`bcdedit /copy {identifer} /d "description"`，`{identifer}`所代表的是identifer所對應的名稱 (單一開機模式時通常為current)；`description`則替換成該開機模式所顯示的名稱。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/52.png)

**當要變更數個有著相同{identifer}的開機模式時，其變更的順序將是從開機載入器所顯示的順序依序被變更。**

1. 看到已順利將項目複製到{一堆亂碼}就代表成功變更。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/53.png) 

1. 再次輸入bcdedit查看目前的狀態。會發現多了一組開機載入器，那便是剛才複製的

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/54.png) 

1. 先將開機模式的名稱修改好進行區別。

指令為︰`bcdedit /set {identifier} description "你要的名稱"`

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/55.png)

1. 接下來可以使用bcdedit來設定不同的開機模式，您也可以前往「執行」、輸入msconfig，由圖像界面來設定開機模式；在此先使用bcdedit指令進行操作。

指令為`bcdedit /set {identifier}` 不同開機模式的參數

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/56.png) 

1. 再度輸入`bcdedit`，確認開機模式是否正確

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/57.png)

1. 接下來再複製一次最一開始的開機模式，並且重新命名

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/58.png)

1. 接下來使用「執行」、輸入「msconfig」

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/59.png)

1. 選擇「進階」、選取你要變更的作業系統，調整開機選項的設定

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/60.png)

1. 重新開機使設定生效，完成的狀態如下

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/61.png) 