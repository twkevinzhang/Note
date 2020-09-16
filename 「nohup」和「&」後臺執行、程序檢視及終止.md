# 「nohup」和「&」後臺執行、程序檢視及終止
###### tags:`Linux` `cmd`
## 參考
 - [[itread01] nohup和&後臺執行，程序檢視及終止](https://www.itread01.com/content/1548984246.html)
 - [[pixnet] 讓command在遠端執行，不因登出而中斷](https://dragonspring.pixnet.net/blog/post/33257496)

### nohup用途
不掛斷地執行命令。

### nohup語法
    nohup [Command] [Arg...] [&]

無論是否將 nohup 命令的輸出重定向到終端，輸出都將附加到當前目錄的 nohup.out 檔案中。

如果當前目錄的 nohup.out 檔案不可寫，輸出重定向到 $HOME/nohup.out 檔案中。

如果沒有檔案能建立或開啟以用於追加，那麼 Command 引數指定的命令不可呼叫。

### & 用途
    在後臺執行

### & 語法
    [Command] &

### nohup與「&」結合
輸入:`nohup rclone size gd104:/ &`，得到:

    [1] 2017

這是該Command的PID，可以讓你kill用。之後你就可以直接繼續輸入別的指令，`rclone`已經在背景執行


### 檢視執行的後臺程序
第一種:`jobs -l`，得到:

    [1]+  2017 Running                 nohup rclone move --transfers=10 --no-traverse gd60c:/Alpha gd104:/Alpha -P &

當你關閉終端後，`nohup`仍會繼續工作，當你開啟其他終端並想檢視時，就必須使用第二種:`ps -ef`，得到:

    UID        PID  PPID  C STIME TTY          TIME CMD
    root         1     0  0 04:39 ?        00:00:01 /usr/lib/systemd/systemd --switched-root --system --deserialize 22
    root         2     0  0 04:39 ?        00:00:00 [kthreadd]
    root         4     2  0 04:39 ?        00:00:00 [kworker/0:0H]
    root         6     2  0 04:39 ?        00:00:00 [ksoftirqd/0]
    root         7     2  0 04:39 ?        00:00:00 [migration/0]
    yourname  2017  1202  2 05:12 pts/0    00:00:01 nohup rclone size gd104:/

### 終止後臺程序
    kill -9 [PID]