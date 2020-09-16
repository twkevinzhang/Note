# 用Dir指令列出Unicode檔名清單
###### tags:`cmd` `Windwos` `dir` `Unicode`

## 參考
 - [[blogspot] 用Dir指令列出Unicode檔名清單](http://pbice.blogspot.com/2010/11/dirunicode.html)

## 情境說明
我原本就知道MS-DOS模式底下的dir指令可以將結果輸出成文字檔，這樣可以很方便的將所有檔案的檔名做成清單。不過，遇到Unicode檔名該如何處理？

## 步驟
1.  先新增一個文字檔 (例如list.txt)，將編碼改成Unicode。

2.  輸入`cmd /u`，以Unicode模式執行。

3.  執行dir指令，dir >> list.txt。如果只想列出檔名、不要日期、路徑等資訊，可以加參數 b。

4.  注意輸出時一定要有2個輸出符號>>，否則會亂碼。

如果需要大量更改檔名，可以配合[Ant Renamer](http://www.antp.be/software/renamer)使用。