# windows-建立啟用或不啟用Hyper-V的開機模式
###### tags:`windows` `開機選單` `安全模式`

## 參考
  - [[pixnet] 如何調整開機選單及進入安全模式](http://george017.pixnet.net/blog/post/111217963-如何調整開機選單及進入安全模式)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/1.png)

## 情境說明
1. [開機選單的名稱編輯](/windows-開機選單的名稱編輯.md)

2. [開機選單的樣式切換](/windows-切換開機選單樣式的方法.md)

3. [關閉Hyper-V虛擬機的方法](/windows-關閉Hyper-V虛擬機的方法.md)

4. **建立啟用/不啟用Hyper-V的開機模式**

5. [一次性進入安全模式的方法](/windows-一次性進入安全模式的方法.md)

6. [將安全模式加入開機選單的方法](/windows-將安全模式加入開機選單的方法.md)

## 事前準備
1. 一個擁有系統管理員權限的帳號![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/2.png)

2. 命令提示字元![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/3.png)

3. msconfig 設定、boot.ini 設定、Windows 功能、Windows 進階啟動![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/4.png)


## 步驟

1. 首先請使用具有系統管理員權限的帳戶登入系統

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/29.png)

1. 以系統管理員身份執行命令提示字元，輸入`bcdedit`以顯示目前的設定

1. 使用下列指令關閉某個開機模式的Hyper-V
```
bcdedit /set {indetifier} hypervisorlaunchtype off
bcdedit /set {indetifier} hypervisorlaunchtype auto
```

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/30.png)
1. 再次輸入bcdedit，看到下圖的結果代表成功設定
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/31.png)

1. 然後嘗試建立一個啟用Hyper-V的開機模式，先以指令複製一個關閉Hyper-V的開機模式(可參考![](/windows-將安全模式加入開機選單的方法.md))；然後以`bcdedit`指令為該模式啟用Hyper-V

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-如何調整開機選單及進入安全模式/32.png)
