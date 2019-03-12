# windows-更改命令提示字元的預設路徑
###### tags:`cmd` `windows` 
 參考至:[https://www.foolegg.com/how-to-change-the-default-path-of-command-prompt-cmd/](https://www.foolegg.com/how-to-change-the-default-path-of-command-prompt-cmd/)

[![更改命令提示字元的預設路徑](https://lh5.googleusercontent.com/Tl1KwkJ8DrsVsO2tvZEepHBeYkslY_ZekBxwWV1LL9RTe3auE8zYtNmws-HQtNJjAdXRaONyZFXdSV002D94d2T79CP596uMdwSce_J6GAjOs393dd9EHs-Gq5uuQqHAlDM9SQGm "更改命令提示字元的預設路徑")](https://www.foolegg.com/how-to-change-the-default-path-of-command-prompt-cmd/)

對於SA來說，如果每次打開命令提示字元Command Prompt (cmd)都需要更改至指定路徑，為什麼不更改命令提示字元的預設路徑呢？這個教學將介紹如何更改命令提示字元的預設路徑。

請確保您的Windows帳戶是擁有「管理員」的權限。或者您擁有「管理員」的密碼並以「管理員」的身份去執行以下內容。想了解更多可以「[按此](https://www.foolegg.com/index.php?p=510)」

### step.1

按下「開始」，輸入「regedit」，然後以系統管理員身份執行「regedit」。Windows XP下按下「開始」，然後按「執行…」，再輸入「regedit」。執行後可以查看及更改登錄檔資料。![以系統管理員身份執行regedit查看及更改登錄檔資料](https://lh4.googleusercontent.com/8lZuZfc777oBAJGDbrAOxO23Tp6VAjNmXmNhM_xSo7MFmPeteWzWrPgQzwA1fPIVB5PvO7tv-Ddf1_3zW_gFuNHcmXTxhzElR5MqjZHcLccXafIancHBkOvoNId4UCGGR-_2X-4v "以系統管理員身份執行regedit查看及更改登錄檔資料")

### step.2

進入「HKEY_CURRENT_USER\Software\Microsoft\CommandProcessor」目錄。並點擊滑鼠右鍵，選擇「新增(N)」內的「字串值(S)」。![進入CommandProcessor](https://lh5.googleusercontent.com/wYEUHIqm5PhrGx5xLNBZEmjEkbGAZNIRm4Yg3cyDcRSG_Q-ayLH1JPEnS1nSmxEg9TVGqU7SQDS8Rg_6fF4i_InbTzEjGom7-KCxL-2BP3peV4tHn5Uk2a880NRF_G0197ZkHhtb "進入CommandProcessor")

### step.3

將新增的字串值命名為AutoRun。

![將字串值命名為AutoRun](https://lh5.googleusercontent.com/9veMCYjbDColHr2VkK-aQrDFsy8GmKy4NQKyUeA7zBWAw4Oc3mlpGzHIjM6g0sBz_IQX_9NK_KVyEAGzb9H5i7QYd0FzbrROtN1Xx2X0b8jOPUZfrpw4q2JwPs4ZbCvVzPACpJbe "將字串值命名為AutoRun")

### step.4

在AutoRun字串值上點擊滑鼠右鍵，選擇「修改(M)…」。

![修改AutoRun字串值](https://lh6.googleusercontent.com/NJd2XjLSL84V2nIiJJBVFtUEUMzXedjHLk5Jpeqo0o1hDRgdKnvD6Hm8oCh0tAPQXmtUpa4ftPBuNPmctxJ-8Z9pjFzG_QUxjP1dUxXWrcDm67bcbCD8I1RMMgxMkpvbgWD8xs0Q "修改AutoRun字串值")

### step.5

修改數值資料為「CD /D <位置>」。例如修改成使用者FoolEgg的桌面是「CD /D C:\Users\FoolEgg\Desktop」。

![修改數值資料](https://lh4.googleusercontent.com/wCsr_MjVaj-rTyCAFI8NvMIX--gr73ELuSISXc7AyXbQMLMMDqIwMxHFhjNfa6YQuFtSU-fL7DKVMzwydT1ytpEfQT4PONhTzPf1zn9FO4X5ZgCegQIVcq8N3ppygJHLnDvyBMzF "修改數值資料")

### step.6

打開「命令提示字元」。

![打開命令提示字元](https://lh4.googleusercontent.com/0u8XQX_mAMJFEVUmPGAaq-e7PqYZSZGPVcVwp8hx6L2IlLn17UtVDooc5hdQ92YXqMiEN_w1aGdz3N3ulAc6Nt9zL_I6H-YphCj8MXVOO_Ej2adpS0IYSSwhIcEqBOc3rBr3NJSJ "打開命令提示字元")

### step.7

上面的是修改前的效果（預設位置），下面的是修改後的效果。

![效果](https://lh4.googleusercontent.com/vAl4u7S0GfrBHopvL-gwhDWGU9oQ5c_V2WCWSeLRm6m6bTiI_Jy7EiL7ANoZIT_9UtLRwXDtnw6Cx2ciMNIWripI8dsSFlozujxkGnHsllz7ORO-NMIB7hz0X8r5zSJiqMJeZMFp "效果")