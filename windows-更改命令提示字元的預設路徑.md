# windows-更改命令提示字元的預設路徑
###### tags:`windows` `cmd`
 參考至:
  - [[教學] 更改 命令提示字元 Command Prompt (cmd) 的預設路徑](https://www.foolegg.com/how-to-change-the-default-path-of-command-prompt-cmd/)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/1.png)

對於SA來說，如果每次打開命令提示字元Command Prompt (cmd)都需要更改至指定路徑，為什麼不更改命令提示字元的預設路徑呢？這個教學將介紹如何更改命令提示字元的預設路徑。

請確保您的Windows帳戶是擁有「管理員」的權限。或者您擁有「管理員」的密碼並以「管理員」的身份去執行以下內容。想了解更多可以「[按此](https://www.foolegg.com/index.php?p=510)」

### step.1

按下「開始」，輸入「regedit」，然後以系統管理員身份執行「regedit」。Windows XP下按下「開始」，然後按「執行…」，再輸入「regedit」。執行後可以查看及更改登錄檔資料。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/2.png)

### step.2

進入「HKEY_CURRENT_USER\Software\Microsoft\CommandProcessor」目錄。並點擊滑鼠右鍵，選擇「新增(N)」內的「字串值(S)」。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/2.png)

### step.3

將新增的字串值命名為AutoRun。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/3.png)

### step.4

在AutoRun字串值上點擊滑鼠右鍵，選擇「修改(M)…」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/4.png)

### step.5

修改數值資料為「CD /D <位置>」。例如修改成使用者FoolEgg的桌面是「CD /D C:\Users\FoolEgg\Desktop」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/5.png)

### step.6

打開「命令提示字元」。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/6.png)

### step.7

上面的是修改前的效果 (預設位置)，下面的是修改後的效果。
![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/windows-更改命令提示字元的預設路徑/7.png)