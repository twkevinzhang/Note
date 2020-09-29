# Excel-群組背景條紋設定教學
###### tags:`Excel`

## 參考
 - [Excel 顏色條紋設定教學，表格列與列之間以不同顏色間隔](https://blog.gtwang.org/windows/excel-alternate-row-column-colors/2/)中「依照儲存格內容判斷顏色」章節

## 情境說明
將幾個列組成群組，並且用條紋背景色顯示，讓資料更好閱讀

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/6.png)
 > 結果圖

## 步驟
1. 開啟含有組別欄位的資料，這裡示範以第二欄的 Plant 作為分組的依據。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/1.png)

2. 在表格的後方新增一個群組欄位，在 G2 儲存格填入類似這樣的公式，將 Plant 的欄位值轉為 0 與 1 的交錯值：
```
=MOD(IF(ROW()=2,0,IF(B2=B1,G1, G1+1)), 2)
```
這裡的 B1、B2 對應的是 Plant 欄位值，而 G1 則是新增的群組欄位。將此公式填入 G2 儲存格之後，用滑鼠拖曳的方式，把這個公式套用至整個新增的群組欄位，就會得到這樣的結果：

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/2.png)

有了新的群組欄位之後，就可以依照這個欄位的數值來填入列的顏色。

3. 選取表格中所有資料（標題列除外）。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/3.png)

4. 設定格式化的條件，新增格式化規則，公式使用：
```
=$G2=0
```

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/4.png)

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/5.png)

5. fin. 套用格式化條件之後，Excel 就會依據新群組欄位來設定每一列的顏色，這樣表格就會以顏色來區分不同的群組，讓資料一目了然。

![](https://raw.githubusercontent.com/neslxzhen/Note/master/img/Excel-群組背景條紋設定教學/6.png)